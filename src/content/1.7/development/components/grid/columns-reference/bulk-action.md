---
title: BulkActionColumn reference
menuTitle: BulkActionColumn
weight: 20
---

# BulkActionColumn Type
{{< minver v="1.7.5" title="true" >}}

This type of column allows to add bulk action checkboxes to your Grid. This only add the checkbox in the grid, you can then manage bulk actions via javascript.

## Available options

| Properties     | Type   | Expected value                                                                    |
| -------------- | ------ | --------------------------------------------------------------------------------- |
| **bulk_field** | string | **required:** Record field name which will be used as bulk action checkbox value. |

## Example usage

```php
use PrestaShop\PrestaShop\Core\Grid\Column\Type\Common\BulkActionColumn;
use PrestaShop\PrestaShop\Core\Grid\Column\ColumnCollection;

$bulkActionColumn = new BulkActionColumn('bulk_action');
$bulkActionColumn->setName(''); // it is common set empty name for bulk action columns
$bulkActionColumn->setOptions([
     'bulk_field' => 'id_product',
]);

$columns = new ColumnCollection();
$columns->add($bulkActionColumn);
```