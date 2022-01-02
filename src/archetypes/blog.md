+++ 
title = ""
description = ""
tags = []
categories = []
series = []
authors = ["Tobias Mende"]
featuredImage = "/images/{{ .File.BaseFileName }}.jpg"
date = {{ substr .File.BaseFileName 0 10 }}T11:00:00+01:00
slug = "{{ substr .File.BaseFileName 11 }}"
draft = false
+++
