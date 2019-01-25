# Woocommerce
#How to show product image in receipt mail

Copy & paste this code in functions.php file


add_filter( 'woocommerce_email_order_items_args', 'email_order_items', 10, 1 );
 
function email_order_items( $args ) {
 
    $args['show_image'] = true;
    $args['image_size'] = array( 100, 100 );
 
    return $args;
 
}
