Laravel Blade:

- Blade is Laravel's templating engine.
- Blade allows you to write HTML code and embed PHP code using Blade syntax.
- Blade templates are stored in the resources/views directory.
- Blade templates have a .blade.php extension.

Blade Syntax:

- {{ }}: Echoes a PHP variable or expression.
- <?= ?>: Short syntax for {{ }}.
- @: Used for Blade directives (e.g., @if, @foreach, @include).
- {{ }}: Used for PHP code and variables.

Blade Directives:

- @if: Conditional statement.
- @elseif: Else if statement.
- @else: Else statement.
- @foreach: Loop through an array or collection.
- @for: Loop through a range of numbers.
- @include: Include another Blade template.
- @yield: Yield content to a section.
- @section: Define a section.
- @stop: Stop executing the template.

Blade Example:

<!-- resources/views/home.blade.php -->

<h1>{{ $title }}</h1>

<ul>
    @foreach ($items as $item)
        <li>{{ $item }}</li>
    @endforeach
</ul>

@if ($condition)
    <p>This is true!</p>
@endif

Blade allows you to separate your presentation logic from your application logic, making your code more organized and maintainable.