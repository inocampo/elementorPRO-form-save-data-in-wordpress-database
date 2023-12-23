add_action( 'elementor_pro/forms/new_record', function( $record, $ajax_handler ) {
    
    $raw_fields = $record->get( 'fields' );
    $fields = [];
    foreach ( $raw_fields as $id => $field ) {
        $fields[ $id ] = $field['value'];
    }
    
    global $wpdb;
    $output['success'] = $wpdb->insert('demo', array( 'name' => $fields['name'], 'email' => $fields['email'], 'message' => $fields['message']));
    
    $ajax_handler->add_response_data( true, $output );
    
}, 10, 2);
