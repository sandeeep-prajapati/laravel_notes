Pagination in Laravel:

- Use the paginate method to retrieve paginated results:

$users = User::paginate(10);

- In your Blade template, use the links method to display pagination links:

{{ $users->links() }}

- You can also use the following variables in your Blade template:
    - {{ $users->firstItem() }}: First item of the current page
    - {{ $users->lastItem() }}: Last item of the current page
    - {{ $users->total() }}: Total number of items
    - {{ $users->perPage() }}: Number of items per page
    - {{ $users->currentPage() }}: Current page number
    - {{ $users->hasMorePages() }}: Check if there are more pages

Example Blade template:

<h1>Users</h1>

<ul>
    @foreach ($users as $user)
        <li>{{ $user->name }}</li>
    @endforeach
</ul>

{{ $users->links() }}

This will display a list of users with pagination links below.

Customizing Pagination Views:

- You can customize the pagination views by creating a new Blade template in the resources/views/vendor/pagination directory.
- Name the template bootstrap-4.blade.php to use the Bootstrap 4 pagination style.
- In your Blade template, use the links method to display pagination links:

{{ $paginator->links('pagination::bootstrap-4') }}

This will use the custom pagination view.