# Examples for the delete_between filter

## Original file
````
line1
del1
del2
line2
del1
del2
line3
````

## Output file
````
line1
del1
del2
line2
line3
````

## Filter
````
filter_lines '/example/delete_between' do
 filters(delete_between: [/^line2$/, /^line3$/, /del/, :last])
end
