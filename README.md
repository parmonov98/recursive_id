# recursive_id
when you want a spesific data numerate with id in order by increase, this method is for you. 

```
function recursiveNameID($user_id, $lastId = 0){
	
	if(!file_exists('orders/' . $user_id . '_' . $lastId . '.json')){
		return $lastId;
	}else{
		$lastId++;
		if(file_exists('orders/' . $user_id . '_' . $lastId . '.json'))
			$lastId = recursiveNameID($user_id, $lastId);
	}
	
	return $lastId;
}
```
