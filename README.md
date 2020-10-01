PHP_cURL
========

$ch = curl_init($url);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
curl_setopt($ch,CURLOPT_SSL_VERIFYPEER,false); 
curl_setopt($ch,CURLOPT_SSL_VERIFYHOST,1);
curl_setopt($ch, CURLOPT_SSLVERSION, 6);
curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_ANY);
curl_setopt($ch,CURLOPT_POSTFIELDS, $data);
$response = curl_exec ($ch);	//print_r($response);		 
if (curl_errno($ch)) {
$error_msg = curl_error($ch);
}				
curl_close ($ch);
