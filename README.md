# Espressonist-teamGit
Capstone Project

Here's what we're tracking schema-wise:
asterisks should have a required validator in the schema

roaster: (ex: Tinker) *
coffee: (ex: Mayogi Rwanda)*
process: (ex: washed, natural, honey, etc)*
variety: (ex: pacamara, gesha)
elevation: (2500) number
roast: (ex: light, medium, dark) 
in: (18g) number*
out: (36g) number*
time (25s) number*
grind (1.5) float*
temp: (200F) number (might wanna do float)*
wedge: (5.7) number
wdt: boolean* (Weiss Distribution Technique in the UI)
rdt: boolean* (Ross Droplet Technique in the UI)
notes: (ex: blueberry, jasmine, cola, sweet, syrupy)
img: (link from a CDN)

Endpoints will require:

Full CRUD on coffee and full CRUD on users. Only admins get full CRUD on users, and that should be reflected in the UI when the dashboard is rendered.

Coffee GET endpoints should include /getall/:user_id, but also "see other coffees" which is /getall that gets EVERYONE's coffee inputs. Only user_id ones should have an "edit" button next to them. Admin gets "edit" button to ALL.

Let's also implement a search that will allow users to search for a specific coffee. The results should be dynamic and change as the user types (which should be an easy implementation as React is a SPA that triggers re-render each time a hook value changes OR based on useEffect). Read up on useEffect dependency useEffect(() => {}, [] if it's evading your mind currently.

This will also need a CDN (content delivery network) to upload the image of the coffee bag and only send the link generated by the CDN into the DB.

Please utilize MaterialUI to style and AWS EC2 instance to deploy.
