<?php
class Thesaurus {
  private $thesaurus;

  public function __construct($thesaurus) {
    $this->thesaurus = $thesaurus;
  }

  public function getSynonyms($word) {
    if (array_key_exists($word, $this->thesaurus)) {
      return json_encode(array(
        "word" => $word,
        "synonyms" => $this->thesaurus[$word]
      ));
    } else {
      return json_encode(array(
        "word" => $word,
        "synonyms" => array()
      ));
    }
  }
}

$thesaurus = new Thesaurus(array(
  "market" => array("trade"),
  "small" => array("little", "compact")
));

echo $thesaurus->getSynonyms("small");
echo $thesaurus->getSynonyms("asleast");
?>
