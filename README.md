#  3-click Flow

3-click flow is python library that generate a url on the basis of attributes like

### vertical [required]

Acritical vertical For example: mobiles vertical is Supported vertical here https://www.newgensearch.com/mobiles?gd=AP1006343&q=[SearchTerm] 


### gd [required]
 
Specifies the GD unique ID which was supplied by the AM.  Yours GD’s is here https://www.newgensearch.com/mobiles?gd=AP1006343&q=[SearchTerm]

### q [optional]

Specific ads term For example: ‘iPhone 13’ In case ‘q’ parameter will not passed, ads will be displayed by vertical. https://www.newgensearch.com/mobiles?gd=AP1006343&q=iPhone 13



### stid [required]


Site ID is only relevant for display and native traffic sources. In those cases, Site ID should include the value of the site id macro, as provided by the media buying

At Taboola platform {site_id} At Outbrain platform {{section_id}}

https://www.newgensearch.com/mobiles?gd=AP1006343&q=iPhone 13&stid=19829201


### R [optional]

A tracing parameter for reporting. Should contain up to 30 alphanumeric characters. No special characters are allowed other than ‘-’. The number of unique tracing ‘R’ values is limited to 10,000 unique values per implementation per day. Please discuss this with your Account Manager. To 10,000 unique values per implementation per day. Please discuss this with your Account Manager.

https://www.newgensearch.com/mobiles?gd=AP1006343&q=[SearchTerm]&r=14999rc333


### pb [optional]

Media Buy postback encoded URL that may contain all the tracing parameters information. The pb URL will be fired for each user Ad Click action (Server2 Server)
For example:  https://www.mediabuying.com?clickid=2da3fs455a 

1. First it will generate `url` for `newgensearch.com`
2. Opens a browser
3. Clicks on ads 1 by one that will appear after page loading

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install requirements.

```bash
pip install -r requirements.txt
```

## Usage

```python
from actions.click_action import ClickActions


action = ClickActions()

action.perform_3_click("mobiles", "AP1006343", "19829201",)
action.stop()
```