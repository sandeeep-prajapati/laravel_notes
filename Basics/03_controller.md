Laravel Controllers:

- Controllers handle HTTP requests and interact with models and views.
- Controllers are stored in the app/Http/Controllers directory.
- Basic Controller:

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class HomeController extends Controller
{
    public function index()
    {
        return view('home');
    }
}

- Controller Methods:
    - index(): Handles GET requests to "/"
    - create(): Handles GET requests to "/create"
    - store(): Handles POST requests to "/"
    - show(): Handles GET requests to "/{id}"
    - edit(): Handles GET requests to "/{id}/edit"
    - update(): Handles PUT/PATCH requests to "/{id}"
    - destroy(): Handles DELETE requests to "/{id}"
- Dependency Injection:

public function __construct(UserRepository $users)
{
    $this->users = $users;
}

- Middleware:

public function __construct()
{
    $this->middleware('auth');
}

- Resource Controllers:

shell
php artisan make:controller PhotoController --resource

- Controller Helpers:

use Illuminate\Http\Response;

return response()->view('home');

These are the basics of controllers in Laravel. Let me know if you need more information or examples!