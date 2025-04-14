2025-01-21 09:43

### Status:  #baby 

### Tags: [[blab]] [[data-engineering]]

# Google Tag Manager 

Google Tag Manager is the tool used by analytics and developers to create tracking methods for an specific application. It allows analytics to create it's own tracking metrics without much help and time consumption from the developer team.


## Starting

You need an [account] and a [container]. One account can have multiple containers, and a container can be used to multiple websites, but it is recommended that if the sites are really different from each other to use separate containers.

There is a versioning capability also, so in case something breaks on a published container you can rollback the changes.
On Admin section, you can find the install code and you can export and import container configurations.

**Google Tag Manager code must be added to all pages of the website**

### Tags, triggers and variables

#### Tags
Pieces of code that will fire based on the conditions set on GTM

#### Triggers
Are what define *when* the tags are fired. It is a set of conditions that must be met, and when they happen, the tag linked to the trigger will be fired.

#### Variables
Specify the exact when/what/how the trigger will be set, so you can for example add a regex component to it from a page url.

![[Pasted image 20250121100822.png]]

![[Pasted image 20250121101347.png]]

You can mix variables in both tags and triggers, so in this example we have a variable that triggers the Tag, and at the same time the variable in the tag maps the $ of purchase


--------

[[2025-02-10]]

- how many microsecs an user is on the page
- actions people are taking
	- which actions?
- clicks
- were the users are using from
	- browser optmization
- views before completion
	- people getting stuck
	- infer going/moving pages
	- page_referrer





# References

https://www.youtube.com/watch?v=JeFPvUehQ-E







