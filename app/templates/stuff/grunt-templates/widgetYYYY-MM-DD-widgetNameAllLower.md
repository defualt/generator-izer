---
layout: post
title: "<%= widgetNameFirstCap %>"
description: ""
category: 
tags: [dev]
git_widget_repo_name: "<%= widgetNameAllLower %>"
---

{x% include JB/setup %x}

description

{x% include BE/github_widget %x}

<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/<%= widgetNameAllLower %>/css/<%= widgetNameAllLower %>.css" media="screen" type="text/css" />
<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/<%= widgetNameAllLower %>/css/app.css" media="screen" type="text/css" />
<div class="<%= widgetNameAllLower %>BlogWidgetWrap widgetWrap">
	<div class="<%= widgetNameAllLower %>WidgetFrame"> </div>
</div>
<script> 
	inlineScript.<%= widgetNameAllLower %> = require.config({
		paths: {
	 		'jQuery': '{{ site.JB.WIDGET_PATH }}/<%= widgetNameAllLower %>/bower_components/jquery/jquery.min'
	 	},
	 	shim: {
	        'jQuery': {
	            exports: '$'
	        }
	    },
     	 context: "<%= widgetNameAllLower %>",
         baseUrl: "{{ site.JB.WIDGET_PATH }}/<%= widgetNameAllLower %>/"
    });
	inlineScript.<%= widgetNameAllLower %>(['js/app']);
</script>