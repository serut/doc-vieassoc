## Informations

We modified a litle bit the Laravel template for reducing the compilation time on each request.

If you modified a file on /app/views/template/* that is not /app/views/template/**theme.blade.php**, the modification will not operate because Laravel will not detect the modification and will not refresh caches files.

You will need to save ( even without modification ) the /app/views/template/**theme.blade.php** for allowing Laravel  to refresh views in /app/views/template/* that needs to be refreshed.