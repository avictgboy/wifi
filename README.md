# WiFi Billing System with MikroTik Integration

This is an automated WiFi card selling system integrated with MikroTik router. The system allows users to purchase WiFi access packages through bKash payment and automatically receives access credentials.

## Features

- Multiple WiFi packages with different durations
- Automated bKash payment processing
- MikroTik router integration for automatic user creation
- SMS notification system
- Admin dashboard for package and transaction management
- Detailed reports and analytics

## Requirements

- PHP 8.1 or higher
- Laravel 10.x
- MySQL 5.7 or higher
- MikroTik Router with API access enabled
- SMS Gateway API access
- bKash Merchant API access

## Installation

1. Clone the repository:
```bash
git clone [repository-url]
cd wifi-billing-system
```

2. Install dependencies:
```bash
composer install
```

3. Create and configure environment file:
```bash
cp .env.example .env
```

4. Generate application key:
```bash
php artisan key:generate
```

5. Configure database in .env file:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=wifi_billing
DB_USERNAME=root
DB_PASSWORD=
```

6. Configure MikroTik settings in .env file:
```
MIKROTIK_HOST=192.168.1.1
MIKROTIK_USER=admin
MIKROTIK_PASSWORD=your_password
MIKROTIK_PORT=8728
```

7. Configure SMS Gateway settings in .env file:
```
SMS_API_KEY=your_api_key
SMS_SENDER_ID=your_sender_id
```

8. Configure bKash API settings in .env file:
```
BKASH_API_KEY=your_api_key
BKASH_API_SECRET=your_api_secret
BKASH_USERNAME=your_username
BKASH_PASSWORD=your_password
```

9. Run database migrations:
```bash
php artisan migrate
```

10. Start the development server:
```bash
php artisan serve
```

## Usage

### Admin Panel

1. Access the admin panel at `/admin`
2. Create WiFi packages with different durations and prices
3. Monitor transactions and verify payments
4. View reports and analytics

### Customer Purchase Flow

1. Customer visits the homepage
2. Selects a WiFi package
3. Makes payment through bKash
4. Submits payment information
5. Receives WiFi credentials via SMS

## MikroTik Configuration

1. Enable API access on your MikroTik router
2. Create a user profile for API access
3. Configure hotspot server
4. Set up user profiles matching the package durations

## Security

- Keep your .env file secure and never commit it to version control
- Use strong passwords for all services
- Regularly update your dependencies
- Monitor system logs for suspicious activities

## Troubleshooting

1. If MikroTik connection fails:
   - Verify router IP address and credentials
   - Check if API access is enabled
   - Ensure firewall allows API connections

2. If SMS sending fails:
   - Verify API credentials
   - Check SMS balance
   - Verify phone number format

3. If payment verification fails:
   - Check bKash API credentials
   - Verify merchant account status
   - Check transaction logs

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.