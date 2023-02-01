
# Create a new static page on MBAKids App

This tutorial demonstrates how to create a new page in the MBAKids web application. 
To do this, we will create a blade file and define a function in the FrontendController
to render it. Finally, we will define a route to access the page.

 


## 1. Blade file:

a. Create a new blade file in the directory

`/core/resources/views/front/mbakids/pages/`

Name the file "exemplu.blade.php".

b. Add the following code to the blade file:

```php
@extends('front.mbakids.layout.mba-kids-simple')
@section('sub_banner')
<div class="banner-part sub-page-banner ic_banner_subpart">
  <div class="sub-banner ic_sub_baner">
    <div class="container">
      <h1> Titlu Curs </h1>
    </div>
  </div>
  <img class="ic_banner_image" src="https://cdn.mbakids.ro/assets/mbakids/images/banner.svg" alt="Imagine banner mbakids.ro" />
</div>
@endsection
@section('content')
    <section class="ic_section_some_name">
        //  Content of section 
    </section>
    <section class="ic_section_some_other_name">
        //  Content of section 
    </section>
    @include('front.mbakids.parts.contact-form-selling')
    @include('front.mbakids.parts.newsletter')
    @section('seo')
        <title>  </title> 
        <meta name="description" content=""> 
        <link rel="canonical" href=""> 
        <meta name="author" content=""> 
        <meta name="keywords" content=""> 
        <meta property="og:image" content=""> 
        <meta property="og:title" content=""> 
        <meta property="og:url" content="">
        <meta property="og:description" content=""> 
        <meta property="og:type" content=""> 
        <meta property="og:site_name" content=""> 
        <meta name="twitter:title" content=""> 
        <meta name="twitter:description" content=""> 
        <meta name="twitter:image" content=""> 
        <meta name="twitter:site" content="@"> 
        <meta name="twitter:creator" content="@"> 
        <meta name="twitter:url" content=""> 
        <meta name="twitter:card" content="">
    @endsection
@endsection
```

## 2. FrontendController:

a. Open the file 
`/core/app/Http/Controllers/Front/FrontendController.php`

Name the file "exemplu.blade.php".

b. Add the following code to the FrontendController:

```php
public function exemplu()
{
    return view('front.mbakids.pages.exemplu');
}
```

## 3. Route:

a. Open the file 
`/core/routes/web.php`

Name the file "exemplu.blade.php".

b. Add the following code to the file:

```php
Route::get('/exemplu', 'Front\FrontendController@exemplu')->name('front.mbakids.pages.exemplu');
```

## Tech Stack

**Client:** Blade, Laravel 7, Bootstrap CSS, JQuery

**Server:** PHP, Apache2


## Lessons Learned

With these steps completed, you should now have access to the https://mbakids.ro/exemplu.

This is a simplified version of page management.

Other existing pages use dynamic properties such as dynamic meta, dynamic content, and can be updated to access relevant information from the database.

## Support

For support, email razvan@ideacat.ro.


## Others


🤔 Looking for help with...

💬 Ask me about...

📫 How to reach me...

