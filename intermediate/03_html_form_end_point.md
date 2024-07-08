Here's an example of an HTML form with different methods and how to handle them in a Laravel controller:

HTML Form:

<!-- GET method -->
<form action="{{ route('form.get') }}" method="get">
    <input type="text" name="name">
    <button type="submit">Submit (GET)</button>
</form>

<!-- POST method -->
<form action="{{ route('form.post') }}" method="post">
    @csrf
    <input type="text" name="name">
    <button type="submit">Submit (POST)</button>
</form>

<!-- PUT method -->
<form action="{{ route('form.put') }}" method="post">
    @csrf
    @method('put')
    <input type="text" name="name">
    <button type="submit">Submit (PUT)</button>
</form>

<!-- DELETE method -->
<form action="{{ route('form.delete') }}" method="post">
    @csrf
    @method('delete')
    <button type="submit">Submit (DELETE)</button>
</form>

Laravel Controller:

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class FormController extends Controller
{
    public function get(Request $request)
    {
        // Handle GET request
    }

    public function post(Request $request)
    {
        // Handle POST request
    }

    public function put(Request $request)
    {
        // Handle PUT request
    }

    public function delete(Request $request)
    {
        // Handle DELETE request
    }
}

Routes:

Route::get('/form/get', 'FormController@get')->name('form.get');
Route::post('/form/post', 'FormController@post')->name('form.post');
Route::put('/form/put', 'FormController@put')->name('form.put');
Route::delete('/form/delete', 'FormController@delete')->name('form.delete');

Note: The @csrf directive is used to generate the CSRF token in the form, and the @method directive is used to specify the HTTP method (PUT or DELETE) in the form.