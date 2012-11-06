nokogiri_xml_parser
===================

The above ruby code is to parser any XML file and to retrive particular information which you want


INSTALL:
========

To use this rubygem:
```
sudo gem install nokogiri
```

REQUIREMENTS:
=============

*Ruby (tested with 1.9.3 and 1.8.1)

*nokogiri

USAGE:
=======

```
Sample File (file.xml)

<name>
  <boy>
    <array>
      <string> jabacs </string>
      <string> csjaba </string>
      <string> jawahar.c.s </string>
    </array>
  </boy>
</name>
```
```ruby
  require 'nokogiri'
  require 'open-uri'
  # Get a Nokogiri::HTML::Document for the page we’re interested in...
  @doc = Nokogiri::XML(File.open("file.xml"))

  @doc.xpath('//string').each do |link|
    ids << link.content
  end
```


expect output:
=============
'''
jabacs
csjaba
jawahar.c.s
'''



