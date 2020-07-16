# php
$persons = ["გიორგი ჯიბლაძე", "გიორგი გაგოშიძე", "გეგი ფირცხალავა"];
usort($persons, function ($a, $b) {
   $parts_a = explode(' ', $a);
   $last_a  = array_pop($parts_a);
   array_unshift($parts_a, $last_a);
   $a = implode(' ', $parts_a);
   $parts_b = explode(' ', $b);
   $last_b  = array_pop($parts_b);
   array_unshift($parts_b, $last_b);
   $b = implode(' ', $parts_b);
   return strcasecmp($a, $b);
});
print_r($persons);
exit();
