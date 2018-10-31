# CloudThemes

## Cloud Arr
The current version has support for Radarr, Sonarr V2, Sonarr V3, Lidarr, and Bazarr

### Setup
<details><summary>Expand</summary>
<p>
Radarr and Sonarr don't give you an easy way to add custom css, so you will need to insert it with your reverse proxy. The below is an example that you can inside your NGINX Sonarr and Radarr location blocks to insert the CSS when accessing via your domain (not locally). You need the subfilter module for it to work. If you don't use nginx or don't have that module, I don't know enough to help out.

```nginx		
			proxy_set_header Accept-Encoding "";
			sub_filter
			'</head>'
			'<link rel="stylesheet" type="text/css" href="https://rg9400.github.io/CloudThemes/CloudArr.css">
			</head>';
			sub_filter_once on;
 ```
 </p>
</details>

## Cloud Tautulli
The current version supports Tautulli

### Setup
<details><summary>Expand</summary>
<p>
Tautulli doesn't give you an easy way to add custom css, so you will need to insert it with your reverse proxy. The below is an example that you can inside your NGINX Tau location block to insert the CSS when accessing via your domain (not locally). You need the subfilter module for it to work. If you don't use nginx or don't have that module, I don't know enough to help out.

```nginx		
			proxy_set_header Accept-Encoding "";
			sub_filter
			'</head>'
			'<link rel="stylesheet" type="text/css" href="https://rg9400.github.io/CloudThemes/CloudTau.css">
			</head>';
			sub_filter_once on;
 ```
  </p>
</details>
