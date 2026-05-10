# Sprint 6 - Acceptance and Regression Test Analysis

## Part 1 - Analyze the Change

### Newly Implemented Functionality

Based on the Sprint Goal and implemented user stories, the following
new functionality was introduced:

- Czech language support
- Czech product/article localization
- Integration of Czech payment provider `PayU`
- Marketplace preparation for `Alza.cz`
- New authentication library `xauth-X64`
- Password hashing implementation
- Security improvements in authentication handling

---

## Changed Functionality

The following existing functionality was modified:

- Checkout workflow
- Payment selection and payment processing
- Authentication and login handling
- Registration and password management
- Product information management
- Localization and language handling
- Customer-facing webshop navigation

---

## Potentially Impacted Existing Features

The following existing features may be impacted by the changes:

- User registration
- User login/logout
- Password reset
- Product search
- Product details
- Shopping cart
- Checkout flow
- Payment processing
- Order confirmation
- Customer profile handling
- Session management

---

## Critical Business Workflows

### Business-Critical Workflows
- Customer registration
- Customer login
- Product purchase
- Checkout and payment
- Order placement
- Marketplace product synchronization
- Multi-language product presentation

---

## Integration Points

### External Integrations
- `PayU Czech Republic`
- `Alza.cz Marketplace`

### Internal Integrations
- Authentication service
- Session management
- Product catalog
- Checkout workflow
- Payment workflow
- Localization framework

---

## Risk Areas

### Functional Risks
- Incorrect language switching
- Broken checkout process
- Payment failures
- Missing product translations
- Authentication instability

### Security Risks
- Weak password handling
- Session manipulation
- Authentication bypass
- Broken login sessions
- Insecure payment communication

### Regression Risks
- Existing users unable to log in
- Existing checkout workflow broken
- Product search impacted by localization
- Cart persistence issues
- Existing payment methods affected

---

# Part 2 - Define the Test Scope

## Acceptance Testing Scope

The following functionality requires acceptance testing:

- Czech language support
- Czech product content
- PayU payment integration
- Updated authentication library
- Password hashing implementation
- Czech checkout workflow

---

## Regression Testing Scope

The following existing functionality requires regression testing:

- Existing login functionality
- Registration workflow
- Password reset
- Shopping cart handling
- Existing checkout process
- Existing payment methods
- Product search and filtering
- Order confirmation workflow
- Session handling

---

## Most Critical Business Processes

### Highest Priority
- Customer authentication
- Checkout and payment
- Order placement

### Medium Priority
- Product localization
- Marketplace preparation
- Customer profile handling

---

## Prioritized Risks

### High Priority Risks
- Login failure after authentication migration
- Checkout failure with new payment integration
- Security vulnerabilities in session handling
- Payment transaction failures

### Medium Priority Risks
- Broken localization
- Incorrect product translations
- Cart persistence issues

### Low Priority Risks
- UI inconsistencies
- Minor translation issues

---

# Part 3 - T1&T5 Test Set

## Selected Use-Case

### Customer completes checkout using Czech localization and PayU payment

The use-case includes:
- Czech language selection
- Product selection
- Shopping cart handling
- Checkout execution
- PayU payment processing
- Order confirmation

---

# T1 Test Titles

- T1_Localization_CzechLanguageSelection_CzechContentDisplayed
- T1_ProductCatalog_CzechProductInformation_LocalizedProductDisplayed
- T1_ShoppingCart_ValidProductSelection_ProductAddedSuccessfully
- T1_Checkout_ValidCheckoutData_CheckoutProcessedSuccessfully
- T1_Payment_ValidPayUPaymentSelection_PaymentAccepted
- T1_OrderConfirmation_SuccessfulCheckout_OrderConfirmationDisplayed
- T1_Authentication_ValidCustomerLogin_LoginSuccessful
- T1_Security_ValidPasswordHashing_AuthenticationProcessedSuccessfully

---

# T2 Test Titles

- T2_Localization_LanguageSwitchDuringCheckout_CheckoutStatePersisted
- T2_Checkout_MultipleLocalizedProducts_OrderProcessedSuccessfully
- T2_Payment_PayUPaymentWithExistingCustomer_OrderProcessedSuccessfully
- T2_ShoppingCart_ReturnFromPayment_CartContentPersisted
- T2_Authentication_LoginAfterPasswordMigration_LoginSuccessful
- T2_ProductCatalog_FilterLocalizedProducts_FilterResultsDisplayed
- T2_Checkout_DifferentBillingAndShippingAddress_OrderProcessedSuccessfully
- T2_Localization_CzechSpecialCharacters_ProductInformationDisplayedCorrectly

---

# T3 Test Titles

- T3_Localization_MissingCzechTranslation_FallbackLanguageDisplayed
- T3_Payment_InvalidPayUPaymentCallback_ErrorHandledGracefully
- T3_Checkout_ExpiredSessionDuringCheckout_ReauthenticationRequired
- T3_Authentication_InvalidPasswordAfterMigration_LoginRejected
- T3_Checkout_EmptyShoppingCart_CheckoutPrevented
- T3_Payment_PaymentCancellationDuringCheckout_OrderNotProcessed
- T3_Localization_InvalidLanguageSelection_DefaultLanguageDisplayed
- T3_Security_InvalidSessionToken_AccessRejected

---

# T4 Test Titles

- T4_Checkout_HighConcurrentPayUPayments_OrdersProcessedReliably
- T4_Localization_HighConcurrentLanguageSwitching_ContentDisplayedCorrectly
- T4_Authentication_HighConcurrentLogins_AuthenticationProcessedReliably
- T4_Checkout_PaymentServiceDelay_CheckoutHandledGracefully
- T4_ProductCatalog_LargeLocalizedCatalog_ResponseTimeWithinThreshold
- T4_Checkout_MobileCheckoutWithLocalization_ResponsiveLayoutDisplayed
- T4_Authentication_SessionTimeoutHandling_UserSessionHandledCorrectly
- T4_Checkout_HighSystemLoad_OrderProcessedSuccessfully

---

# T5 Test Titles

- T5_Authentication_SessionManipulationAttempt_AccessBlocked
- T5_Authentication_BruteForceLoginAttempt_ProtectionMechanismTriggered
- T5_Security_InvalidPasswordHashManipulation_RequestRejected
- T5_Payment_InvalidPayUCallbackManipulation_RequestRejected
- T5_Checkout_OrderPriceManipulation_RequestRejected
- T5_Localization_CrossSiteScriptingInTranslationInput_MaliciousScriptSanitized
- T5_ProductCatalog_SQLInjectionInLocalizedSearch_AttackPrevented
- T5_Authentication_UnauthorizedPrivilegeAssignment_AccessDenied