# Easy Verification

A simple Flutter package for sending and verifying OTP codes via email using Resend service.

## Features

- ✅ Send OTP codes via email
- ✅ Verify OTP codes with expiration
- ✅ Multiple attempt protection
- ✅ Easy Resend integration
- ✅ Beautiful email templates

## Installation

Add to your `pubspec.yaml`:

```yaml
dependencies:
  easy_verification: ^1.0.0
```

```dart
import 'package:easy_verification/easy_verification.dart';

final config = EmailConfig(
  apiKey: 'your_resend_api_key',
  fromEmail: 'onboarding@resend.dev',
);

final otpManager = OTPManager(emailConfig: config);

// Send OTP
final result = await otpManager.sendOTP('user@example.com');

// Verify OTP
final isValid = otpManager.verifyOTP('user@example.com', '123456');
```
