# -Person1-has-several-containers-each-with-a-number-of-balls
Assignment

<?php

function sortBalls($containers) {
    
    $ballCounts = array_count_values($containers);

    
    $containerCounts = array_count_values($ballCounts);

    
    foreach ($containerCounts as $count) {
        if ($count % 2 !== 0) {
            return "Impossible to sort the balls.";
        }
    }

    return "Possible to sort the balls.";
}

$containers1 = [1, 1, 2, 2];
$containers2 = [1, 1, 2, 3];

echo sortBalls($containers1) . "\n"; 
echo sortBalls($containers2) . "\n"; 

?>

