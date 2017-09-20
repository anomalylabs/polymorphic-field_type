## Usage[](#usage)

This section will show you how to use the field type via API and in the view layer.


### Setting Values[](#usage/setting-values)

You can set the polymorphic field type value with a model instance:

    $entry->example = $entry;

You can also set the polymorphic field type value with a decorated model:

    $entry->example = $decorated;


### Basic Output[](#usage/basic-output)

The polymorphic field type always returns `null` or an `\Anomaly\Streams\Platform\Entry\EntryInterface` instance.

###### Example

    $entry->example->getId();

###### Twig

    {{ entry.example.id }}


### Presenter Output[](#usage/presenter-output)

When accessing the field value from a decorated entry model the an instance of `\Anomaly\Streams\Platform\Entry\EntryPresenter` will be returned.

###### Example

    $decorated->example->test;

###### Twig

    {{ decorated.example.test }}
