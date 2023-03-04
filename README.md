## Installation
```
composer require devinow/http
```
## Usage

### Response headers

 * Retrieving a header (with optional value prefix)

   ```php
   $header = \Devinow\Http\ResponseHeader::get('Content-Type');
   // or
   $header = \Devinow\Http\ResponseHeader::get('Content-Type', 'text/');
   ```

 * Setting a header (overwriting other headers with the same name)

   ```php
   \Devinow\Http\ResponseHeader::set('X-Frame-Options', 'sameorigin');
   ```

 * Adding a header (preserving other headers with the same name)

   ```php
   \Devinow\Http\ResponseHeader::add('Vary', 'User-Agent');
   ```

 * Removing a header (with optional value prefix)

   ```php
   $success = \Devinow\Http\ResponseHeader::remove('X-Powered-By');
   // or
   $success = \Devinow\Http\ResponseHeader::remove('X-Powered-By', 'PHP');
   ```

 * Retrieving and removing a header at once (with optional value prefix)

   ```php
   $header = \Devinow\Http\ResponseHeader::take('Set-Cookie');
   // or
   $header = \Devinow\Http\ResponseHeader::take('Set-Cookie', 'mysession=');
   ```