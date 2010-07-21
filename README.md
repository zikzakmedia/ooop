<img src="http://github.com/lasarux/ooop/raw/master/artwork/ooop.png" width="100px" height="100px" />

**Warning: this is a very initial release.**


Contacting us:
--------------------

Discussion group:  [openerp-ooop](http://groups.google.es/group/openerp-ooop?hl=en&pli=1)
Post Issues on github: [GITHUB Issues](http://github.com/lasarux/ooop/issues)
  

Examples (python console):
========================

Connecting to server
--------------------
  <pre><code>from ooop import OOOP
  o = OOOP(dbname='demo')</code></pre>


Retrieving all from model
-------------------------

  from ooop import OOOP
  o = OOOP(dbname='demo')
  o.res_partner.all()

Retrieving 1 record from model
-------------------------

  from ooop import OOOP
  o = OOOP(dbname='demo')
  n = o.res_partner.get(1)

Accesing attributes
--------------------

  from ooop import OOOP
  o = OOOP(dbname='demo')
  n = o.res_partner.get(1)
  print n.name

or in related objects
  
  print n.address.name

Filtering
---------

  o.res_partner.filter(name='Pedro')


Creating new
------------

  n = res_partner.new()
  n.name = 'Partner created with OOOP'
  n.save()

**with related objects**

  n = res_partner.new()
  n.name = 'Partner created with OOOP'

  addr = res_partner_addres.new()
  addr.street = "Testing related objects"
  addr.save()

  n.address = [addr]
  n.save()



comming soon
============

n.save_all() <- to save related objects

-----------------------------------

TODO: to write a better README. ;-)

