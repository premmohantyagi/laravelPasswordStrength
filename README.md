## laravelPasswordStrength
This package provides a validator that ensures strong passwords in Laravel 6 applications.
The provided validations include:

- check if input contains alphabetic characters
- check if input contains numeric characters
- check if input contains mixed case characters
- check if input contains symbols

## Installation
### Get the package
Just ```composer require premmohantyagi/password-strength```.


## Usage
Now Laravel's native `Validator` is extended by four rules:

- case_diff
- numbers
- letters
- symbols

### Example
You can apply these rules as described in the [validation section on Laravel's website](http://laravel.com/docs/validation)

```php
/**
 * Get the validation rules that apply to the request.
 *
 * @return array
 */
public function rules()
{
    return [
        'name'     => 'required|string|max:100',
        'email'     => 'required|string|unique:users|max:255',
        'password'  => 'required|string|min:8|confirmed',            
        'password' => 'case_diff|numbers|letters|symbols', //12345QWERTqwert@        
    ];

}

 /**
 * Custom message for validation
 *
 * @return array
 */
public function messages()
{
    return [
        'name.required'    => 'last name is required!',
        'email.required'    => 'Email is required!',
        'password.required' => 'Password is required!',           
        'password.required' => 'case_diff|numbers|letters|symbols'
    ];
}

```


# History
**[Laravel 6]**


# License

This package is under the MIT license. See the complete license:
- [LICENSE](https://github.com/premmohantyagi/laravelPasswordStrength/LICENSE)


## Reporting Issues or Feature Requests
Issues and feature requests are tracked on [GitHub](https://github.com/premmohantyagi/laravelPasswordStrength/issues).
