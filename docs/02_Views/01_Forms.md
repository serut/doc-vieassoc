**VieAssociative** provide some syntax sugar for creating forms.
We created these methods for using in a fast and maintenable way the Laravel Form component in a Bootstrap HTML structure.

First, you implement an array :

    // Somewhere in a view of Laravel
    @input = array(
            //Here goes all the configuration for the Laravel Form
    		'form' => array(
                //Here goes all the configuration for the Bootstrap structure
    		),
            'elements' => array(
                //Here goes all the configuration for radio and checkbox
            )
        )
    @

And you call just after the corresponding method

    // And by one of these lines you create the input and the bootstrap structure
    {{ SiteHelpers::create_input($input) }}
    {{ SiteHelpers::create_radio($input) }}
    {{ SiteHelpers::create_checkbox($input) }}
Remember : the '{{' and '}}' is a Blade, the Laravel component for Templating, possibility. It just calls the echo function of PHP of what is between these brackets

## Checkbox

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu. In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium.
<pre>
	@input = array(
        'id'=>'',
        'label'=>'',
        'name'=> '',
        'data-toggle'=> '',
        'form' => array(
            '1'=>array(
                'value'=>'',
                'text'=>'',
            ),
        )
    )@
    {{SiteHelpers::create_checkbox($input)}}
</pre>


## Radio

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus cu. In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium.
- data-toggle On true, display specific id

<pre>
@input = array(
    'id'=>'',
    'label'=>'',
    'name'=> '',
    'data-toggle'=> '',
    'form' => array(
        '1'=>array(
            'value'=>'',
            'text'=>'',
        ),
        '2'=>array(
            'value'=>'',
            'text'=>'',
            'checked'=>true,
        ),
    )
)@
{{SiteHelpers::create_radio($input)}}
</pre>