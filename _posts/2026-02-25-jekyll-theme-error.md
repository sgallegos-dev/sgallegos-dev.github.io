---
layout: post
title: "Jekyll Architect Theme Missing Dependency Error"
date: 2026-02-21
categories: jekyll debugging
tags: jekyll github-pages ruby windows
---

## Context

Running Jekyll locally on Windows using Ruby 3.x.

## Problem

Error:
The architect theme could not be found

## Root Cause

GitHub Pages provides themes internally, but locally the theme gem was not declared.

## Solution

Add to Gemfile:
gem "github-pages", group: :jekyll_plugins

Run:
bundle install

## Takeaways

Local environments must explicitly declare dependencies that GitHub Pages resolves automatically.
