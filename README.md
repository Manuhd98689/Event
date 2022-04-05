# Event

$today = date('Ymd');

       $homeevents = new WP_Query(array(

         'posts_per_page' => -1,

		 'post_type' => 'event',

		 'meta_key' => 'event_dates', /* Field name of value */

		 'orderby' => 'meta_value_num',

		 'order' => 'ASC',

		 'meta_query' => array(

		 array(

		 'key' =>'event_dates' ,

		 'compare' => '>=',

		 'value' => $today,

		 'type' => 'numeric'

		 )

		 )

          )); 
