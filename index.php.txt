<?php
use Twig\Environment;
use Twig\Loader\FilesystemLoader;

require '../vendor/autoload.php';
include '../src/view/index.html.twig';


$loader = new Twig\Loader\FilesystemLoader('../src/view');
$twig = new Twig\Environment($loader);

$products = ['product1', 'product2', 'product3', 'product4', 'product5'];

echo $twig->render('index.html.twig', ['products' => $products]);
