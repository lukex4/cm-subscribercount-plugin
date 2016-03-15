
This plugin integrates a Wordpress site with the Campaign Monitor API, specifically to map a Wordpress option - usable anywhere in the template - to the subscriber count of a Campaign Monitor list. There is an optional caching ability, which reduces the number of requests on the Campaign Monitor API. If you set CMCOUNT_CACHESECONDS to 0, requests won't be cached (inadvisible on a busy site). To output the signature count in your template, use 'echo number_format(get_option(CMCOUNT_OPTIONNAME, 5000));' in a PHP tag. In this example, 5000 is the default value that get_option will output if it can't access the live count - this number can be changed to whatever you'd like, or removed completely.