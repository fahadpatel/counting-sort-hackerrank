# counting-sort-hackerrank
counting sort hacker rank solution
<?php

/*
 * Complete the 'countingSort' function below.
 *
 * The function is expected to return an INTEGER_ARRAY.
 * The function accepts INTEGER_ARRAY arr as parameter.
 */

function countingSort($arr) {
    // Write your code here

$countingSort=array();
$count=count($arr);
$sor_arr=array_unique($arr);
$sor_arr_count=count($sor_arr);

for($i=0;$i<100; $i++ ){
  $countingSort[$i]=0;
}


for($i=0; $i<$count; $i++){
    $int=$arr[$i];
    $in_count=0;
    $countingSort[$int]=$countingSort[$int]+1;  

      
}
return $countingSort;

}

$fptr = fopen(getenv("OUTPUT_PATH"), "w");

$n = intval(trim(fgets(STDIN)));

$arr_temp = rtrim(fgets(STDIN));

$arr = array_map('intval', preg_split('/ /', $arr_temp, -1, PREG_SPLIT_NO_EMPTY));

$result = countingSort($arr);

fwrite($fptr, implode(" ", $result) . "\n");

fclose($fptr);
