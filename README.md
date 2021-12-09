{%- assign item = section.settings -%}

<style>

  .qt-testi{
    padding: 110px 0 90px;
    margin-top: -120px;
    position: relative;
    {% if section.settings.use_bg_img %}
    background: url('{{ section.settings.desktop_bg_img | img_url: "master" }}');
      background-repeat: no-repeat !important;
      background-size: 100% 100%;
      {% endif %}

      {% if section.settings.use_bg_color %}
      background: {{ section.settings.bg_color }};
      {% endif %}
      }
  .qt-testi .container{
    padding: 0 15px;
  }
  .qt-testi__inner {
    padding: {{ section.settings.section_padding }};
  }
  .qt-testi__content {
    padding: {{ section.settings.box_padding }};
    background: {{ section.settings.box_bg }};
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    border-radius: 15px;
    text-align: center;
  }
  .qt-testi__title h2 {
    display: block;
    text-transform: none;
    font-size: 18px;
    line-height: 25px;
    font-weight: 700;
    margin: 0;
    padding: 0;
    padding-top: 5px;
    padding-bottom: 0;
    color: {{ section.settings.title_color }};
  }
  .qt-testi__text p {
    margin: 0 0 5px;
    font-size: 16px;
    line-height: 20px;
    font-weight: 700;
    text-align: center;
    color: {{ section.settings.text_color }};
    font-family: Domine,serif;
  }
  .qt-testi__btn a {
    font-size: 16px;
    line-height: unset;
    font-weight: 700!important;
    display: inline-block;
    margin: 0;
    border-radius: 5px;
    text-decoration: none;
    margin-top: 5px;
    width: {{ section.settings.btn_width }};
    background: {{ section.settings.btn_bg_color }};
    color: {{ section.settings.btn_color }};
  }
  .qt-testi__btn a:hover{
    background: {{ section.settings.hover_btn_bg_color }};
    color: {{ section.settings.hover_btn_color }};
  }
  .qt-testi__small-img span{
    display: flex;
    align-items: center;
    height: {{ section.settings.testi__small_height }};
  }
  .qt-testi__small-img svg{
    height: {{ section.settings.testi__small_height }};
  }
  .qt-testi__small-img img{
    height: {{ section.settings.testi__small_height }};
  }
  .qt-testi__main-title{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    width: 100%;
    padding-top: 20px !important;
    padding-bottom: 50px !important;
    text-align: center;
  }
  .qt-testi__main-title h2{
    font-weight: 700;
    letter-spacing: .03em;
    display: block;
    text-transform: none;
    text-align: center;
    font-size: 40px;
    line-height: 46px;
    margin: 0;
    padding: 0;
    color: {{ section.settings.title_color }};
  }
  .qt-testi__main-title p{
    margin: 10px 0 0 !important;
    font-size: 20px;
    line-height: 25px;
    font-family: Domine;
    color: {{ section.settings.title_color }};
  }
  .qt-testiimage__mobile {
    display: none;
  }
  .qt-testi__inner .row .col-lg-7 {
    padding-left: 50px;
  }
  .qt-testi__inner .row {
    margin-top: -55px;
  }
  .qt-testi__btn-mobile{
    display: none;
  }


  /*  Responsive CSS Start  */
  @media screen and (max-width: 991px) {
    .qt-testi{
      margin-top: -20px;
    }
    .qt-testi_right .row {
      display: flex;
      flex-direction: column-reverse;
    }
    .qt-testi__main-title{
      padding-bottom: 10px !important;
    }
    .qt-testi__main-title h2 {
      font-size: 18px !important;
      line-height: 25px !important;
    }
    .qt-testi__inner {
      padding: 30px 0;
    }
    .qt-testi__main-title p {
      font-size: 16px;
      line-height: 20px;
    }
    .qt-testi__btn-mobile{
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 10px 0 40px;
    }
    .qt-testi__btn-mobile a{
      font-family: Montserrat;
      font-style: normal;
      font-weight: bold;
      font-size: 12px;
      line-height: 15px;
      display: flex;
      align-items: center;
      text-align: center;
      color: #FFFFFF;
      padding: 8px 10px;
      text-transform: uppercase;
      background: #65778A;
      border-radius: 6px;
    }
  }
  @media screen and (max-width: 767px) {

    .qt-testiimage__desktop {
      display: none;
    }
    .qt-testiimage__mobile {
      display: block;
    }
    .qt-testi {
      margin-top: -20px;
      padding: 40px 0 0;
      margin-bottom: 50px;
      background: url('https://cdn.shopify.com/s/files/1/0517/7232/6076/files/WffEB--background_nov3dd.png?v=1636805126') !important;
      background-repeat: no-repeat !important;
      background-size: cover !important;
      background-position: center !important;
    }
    .qt-testi__inner .row {
      margin-top: 0;
    }
    .qt-testi__inner .row .col-lg-7 {
      padding-left: 15px;
    }
    .qt-testi__title h2 {
      font-size: 12px;
      line-height: 18px;
    }
    .qt-testi__text p {
      font-size: 12px;
      line-height: 18px;
    }
    .qt-testi__btn {
      display: none;
    }
    .qt-testi__inner {
      padding: 0;
    }
  }
  /*  Responsive CSS End  */

</style>



<section id="{{section.id}}" class="section-separator">
  <div class="qt-testi">
    <div class="module-container">
      <div class="container">
        <div class="qt-testi__inner">
          <div class="qt-testi__main-title">
            <h2>{{ section.settings.qt_main_title }}</h2>
            <p>{{ section.settings.qt_main_text }}</p>
          </div>
          <div class="qt-testiimagemain">
            <div class="qt-testiimagemain__inner">
              <div class="qt-testiimage__desktop">
                <img src="{{ section.settings.desktop_image | img_url: 'master' }}" />
              </div>
              <div class="qt-testiimage__mobile">
                <img src="{{ section.settings.mobile_image | img_url: 'master' }}" />
              </div>
            </div>
          </div>
          <div class="row">
            <div class="col-lg-5"></div>
            <div class="col-lg-7">
              <div class="row">
                {% for block in section.blocks %}
                <div class="col-lg-4 col-md-4 col-4">
                  <div class="qt-testi__content">
                    <div class="qt-testi__title"><h2>{{ block.settings.qt-testi__title }}</h2></div>
                    <div class="qt-testi__text"><p>{{ block.settings.qt-testi__text }}</p></div>
                    {% if block.settings.show_btn %}
                    <div class="qt-testi__btn"><a href="{{ block.settings.qt-testi__link }}">{{ block.settings.qt-testi__link_text }}</a></div>
                    {% endif %}
                  </div>
                </div>
                {% endfor %}
              </div>
            </div>
          </div>

          <div class="qt-testi__btn-mobile">
            <a href="{{ section.settings.btn_url }}">{{ section.settings.btn_text }}</a>
          </div>

        </div>
      </div>
    </div>
  </div>
</section>

{% schema %}
{
    "name": "HP Testi Section",
    "settings": [
        {
            "type": "header",
            "content": "style"
        },
        {
            "type": "color",
            "id": "bg_color",
            "label": "Background Color",
            "default": "#fff"
        },
        {
            "type": "color",
            "id": "title_color",
            "label": "Title Color",
            "default": "#3d79b8"
        },
        {
            "type": "color",
            "id": "text_color",
            "label": "Text Color",
            "default": "#3d79b8"
        },
        {
            "type": "color",
            "id": "btn_bg_color",
            "label": "Button Background Color",
            "default": "#ffe64b"
        },
        {
            "type": "color",
            "id": "btn_color",
            "label": "Button Text Color",
            "default": "#3d79b8"
        },
        {
            "type": "color",
            "id": "hover_btn_bg_color",
            "label": "Hover Button Background Color",
            "default": "#3d79b8"
        },
        {
            "type": "color",
            "id": "hover_btn_color",
            "label": "Hover Button Text Color",
            "default": "#fff"
        },
        {
            "type": "color",
            "id": "box_bg",
            "label": "Box background color",
            "default": "#e6f5ff"
        },
        {
            "type": "text",
            "id": "section_padding",
            "label":"Section Padding",
            "default":"40px 0",
            "info":"top right bottom left"
        },
        {
            "type": "text",
            "id": "box_padding",
            "label": "Content Box Padding",
            "info":"top right bottom left",
            "default": "10px 0"
        },
        {
            "type": "text",
            "id": "btn_width",
            "label": "Button Width",
            "info":"Please add with in PX"
        },
        {
            "type": "checkbox",
            "id": "use_bg_img",
            "label":"Use Background Image"
        },
        {
            "type": "checkbox",
            "id": "use_bg_color",
            "label":"Use Background Color",
            "default": true
        },
        {
            "type": "image_picker",
            "id":"desktop_bg_img",
            "label":"Background Image Desktop"
        },
        {
            "type": "image_picker",
            "id":"mobile_bg_img",
            "label":"Background Image Mobile"
        },
        {
            "type":"text",
            "id":"qt_main_title",
            "label":"Section Title"
        },
		{
            "type":"text",
            "id":"qt_main_text",
            "label":"Section Text"
        },
		{
            "type": "header",
            "content": "Content Background Image"
        },
		{
            "type": "image_picker",
            "id":"desktop_image",
            "label":"Content Image Desktop"
        },
        {
            "type": "image_picker",
            "id":"mobile_image",
            "label":"Content Image Mobile"
        },
        {
            "type": "text",
            "id":"btn_text",
            "label":"Button Text"
        },
        {
            "type": "url",
            "id":"btn_url",
            "label":"Button URL"
        }
		
    ],
    "blocks": [
        {
            "type": "Imagewithtext",
            "name": "Image with Text",
            "settings": [
                {
                    "type": "text",
                    "id": "qt-testi__title",
                    "label": "Title"
                },
                {
                    "type": "textarea",
                    "id": "qt-testi__text",
                    "label": "Text"
                },
                {
                    "type": "checkbox",
                    "id": "show_btn",
                    "label": "Show Button",
                    "default": false
                },
                {
                    "type": "text",
                    "id": "qt-testi__link_text",
                    "label": "Button Text"
                },
                {
                    "type": "url",
                    "id": "qt-testi__link",
                    "label": "Button Link"
                }
            ]
        }
    ],
    "presets": [
        {
            "name": "HP Testi Section",
            "category": "HP"
        }
    ]
}
{% endschema %}

{% stylesheet %}
{% endstylesheet %}

{% javascript %}
{% endjavascript %}



						HTML:- https://prnt.sc/22f5bad


						How To Include CSS And Js In HTMl:-
						
						<!-- Main CSS file -->
						<link href="assets/css/style.css" media="screen" rel="stylesheet">

						<!-- Main js file -->
   						<script src="assets/js/script.js"></script>		



		
							

						How To Include CSS And Js In Shopify:-
						
						{{ 'theme.css' | asset_url | stylesheet_tag }}

						{{ 'slick.js'  | asset_url | script_tag }}








						Wordpress:-

						How to Download Wordpress Blank Theme:-
						https://underscores.me/




						How to include CSS and JS in Wordpress:-

						In Function.php

						// CSS
						wp_enqueue_style( 'new-style-css', get_template_directory_uri() . '/assets/css/style.css', array());

						// JS
						wp_enqueue_script( 'script', get_template_directory_uri() . '/assets/js/scripts.js', array(), _S_VERSION, true );

						



						Shortcode Print:-
						<?php echo do_shortcode('[name_of_shortcode]'); ?>


						Repeater:-
						
			   <div class="cat-list">
                               <div class="cat-list-main">
                                   <ul>
                                       <?php
						if( have_rows('cat-list','option') )
						{
							while ( have_rows('cat-list','option') ){
								the_row(); ?>
									<li>
										<a href="<?php the_sub_field('cat_link','option')?>"><?php the_sub_field('cat_text','option')?></a>
									</li>
								<?php
							}				
						}
					?>
                                   </ul>
                               </div>
                           </div>







		
How To Create Tamplate In Wordpress:

https://prnt.sc/wkuubt

<?php
/**
 * Template Name: Home-template
 *
 * This is the most generic template file in a WordPress theme
 * and one of the two required files for a theme (the other being style.css).
 * It is used to display a page when nothing more specific matches a query.
 * E.g., it puts together the home page when no home.php file exists.
 *
 * @link https://developer.wordpress.org/themes/basics/template-hierarchy/
 *
 * @package Blank-Wordpress-theme
 */

get_header();
?>

	<main id="primary" class="site-main">
		<h1>hello dear</h1>
	</main><!-- #main -->

<?php
get_footer();
