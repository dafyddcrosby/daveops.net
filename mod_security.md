# mod_security
Created Tuesday 10 October 2017

	<IfModule security2_module>
	# Turn on rule engine and set default action
	SecRuleEngine On
	SecDefaultAction "phase:2,deny,log,status:403"
	</IfModule>

