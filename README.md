![Inventory Banner]
(https://github.com/stevebauman/inventory/blob/master/inventory-banner.jpg)

[![Code Climate](https://codeclimate.com/github/stevebauman/inventory/badges/gpa.svg)](https://codeclimate.com/github/stevebauman/inventory)
[![Travis CI](https://travis-ci.org/stevebauman/inventory.svg?branch=master)](https://travis-ci.org/stevebauman/inventory)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/stevebauman/inventory/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/stevebauman/inventory/?branch=master)
[![Latest Stable Version](https://poser.pugx.org/stevebauman/inventory/v/stable.svg)](https://packagist.org/packages/stevebauman/inventory)
[![Total Downloads](https://poser.pugx.org/stevebauman/inventory/downloads.svg)](https://packagist.org/packages/stevebauman/inventory)
[![License](https://poser.pugx.org/stevebauman/inventory/license.svg)](https://packagist.org/packages/stevebauman/inventory)

## Index

<ul>
    <li>
        <a href="#description">Description</a>
        <ul>
            <li><a href="#requirements">Requirements</a></li>
            <li><a href="#benefits">Benefits</a></li>
        </ul>
    </li>
    <li>
        <a href="docs/INSTALLATION.md">Installation</a>
        <ul>
            <li><a href="docs/INSTALLATION.md#installation-laravel-4">Laravel 4</a></li>
            <li><a href="docs/INSTALLATION.md#installation-laravel-5">Laravel 5</a></li>
            <li>
                <a href="docs/INSTALLATION.md#customize-installation">Customize Installation</a>
                <ul>
                    <li><a href="docs/INSTALLATION.md#i-dont-need-to-customize-my-models">I don't need to customize my models</a></li>
                    <li><a href="docs/INSTALLATION.md#i-want-to-customize-my-models">I need to customize my models</a></li>
                </ul>
            </li>
        </ul>
    </li>
    <li>
        <a href="docs/UPDATES.md">Updates</a>
        <ul>
            <li><a href="docs/UPDATES.md#updating-from-10-to-11">Updating from 1.0.* to 1.1.*</a></li>
            <li><a href="docs/UPDATES.md#updating-from-11-to-12">Updating from 1.1.* to 1.2.*</a></li>
            <li><a href="docs/UPDATES.md#updating-from-12-to-13">Updating from 1.2.* to 1.3.*</a></li>
            <li><a href="docs/UPDATES.md#updating-from-13-to-14">Updating from 1.3.* to 1.4.*</a></li>
            <li><a href="docs/UPDATES.md#upcoming-updates">Upcoming Updates</a></li>
        </ul>
    </li>
    <li>
        <a href="docs/USAGE.md">Usage</a>
        <ul>
            <li><a href="docs/USAGE.md#asking-questions">Asking Questions</a></li>
            <li><a href="docs/USAGE.md#sku-generation">SKU Generation</a></li>
            <li><a href="docs/USAGE.md#suppliers">Suppliers</a></li>
            <li><a href="docs/TRANSACTIONS.md">Transactions</a></li>
            <li><a href="docs/EVENTS.md">Events</a></li>
            <li><a href="docs/USAGE.md#exceptions">Exceptions</a></li>
            <li><a href="docs/USAGE.md#auth-integration">Auth Integration</a></li>
            <li><a href="docs/USAGE.md#misc-functions-and-uses">Misc Functions and Uses</a></li>
        </ul>
    </li>
</ul>

## Description

Inventory is a fully tested Laravel inventory solution. It provides the basics of inventory management using Eloquent such as:

- Inventory item management
- Inventory stock management (per location)
- Inventory stock movement tracking
- Inventory SKU generation
- Inventory supplier management
- Inventory transaction management

All movements, stocks and inventory items are automatically given the current logged in user's ID. All inventory actions
such as puts/removes/creations are covered by Laravel's built in database transactions. If any exception occurs
during an inventory change, it will be rolled back automatically.

Depending on your needs, you may use the built in traits for customizing and creating your own models, or
you can simply use the built in models.

### Requirements

- Laravel 4.* | 5.*
- Laravel's Auth, Sentry or Sentinel if you need automatic accountability

Recommended:

- Venturecraft/Revisionable (For tracking Category and Location changes to stocks)

### Benefits

If you're using the traits from this package to customize your install, that means you have complete flexibility over your own
models, methods (excluding relationship names/type), database tables, property names, and attributes. You can set your
own base model, and if you don't like the way a method is performed just override it.

Sit back and relax, it's nice to have control.