# Akaunting Deployment on AWS

## Architecture
EC2 → Nginx + PHP → RDS MySQL

## Steps
1. Launched EC2 instance (Ubuntu 22.04)
2. Installed Nginx, PHP, Composer
3. Deployed Akaunting in /var/www/
4. Configured Nginx server block
5. Created RDS MySQL instance
6. Updated .env with RDS credentials
7. Connected EC2 app to RDS
8. Verified using migrations and UI

## Database Config
DB_CONNECTION=mysql
DB_HOST=<RDS-ENDPOINT>
DB_PORT=3306
DB_DATABASE=akaunting
DB_USERNAME=admin

RDS inbound rule:
- Port: 3306
- Source: EC2 Security Group ONLY

## CRUD
- Create: Add expense
- Read: View expense
- Update: Edit expense
- Delete: Remove expense

http://16.170.206.79/
