---
title: "Plotly Interactive Plot"
author: "Arjun CS"
date: "`r Sys.Date()`"
output:
  html_document:
    code_folding: hide
    theme: flatly
    toc: true
---

## Overview

This document demonstrates an interactive Plotly plot in an R Markdown webpage.

## Plotly Visualization

```{r plotly-example, echo=FALSE}
# Load necessary libraries
library(plotly)

# Create a sample data frame
data <- data.frame(
  category = c("A", "B", "C", "D", "E"),
  values = c(15, 20, 30, 35, 40)
)

# Generate a bar plot using Plotly
plot <- plot_ly(data, x = ~category, y = ~values, type = 'bar', name = 'Categories') %>%
  layout(title = "Category Value Distribution", 
         xaxis = list(title = "Category"), 
         yaxis = list(title = "Values"))
plot
