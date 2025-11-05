---
type: ProjectLayout
title: A very cool code project
colors: colors-a
date: '2021-10-15'
client: Awesome client
description: >-
  It’s hard to imagine that I’ve that I wrote all this code by myself, probably
  because I worked with an entire team :) but they definitely followed my lead
  most of the time.
featuredImage:
  type: ImageBlock
  url: /images/bg1.jpg
  altText: Project thumbnail image
media:
  type: ImageBlock
  url: /images/bg1.jpg
  altText: Project image
---
import { useEffect } from "react";

export default function TableauViz() {
  useEffect(() => {
    const divElement = document.getElementById("viz1762368155888");
    const vizElement = divElement.getElementsByTagName("object")[0];
    vizElement.style.width = "100%";
    vizElement.style.height = (divElement.offsetWidth * 0.75) + "px";

    const scriptElement = document.createElement("script");
    scriptElement.src = "https://public.tableau.com/javascripts/api/viz_v1.js";
    vizElement.parentNode.insertBefore(scriptElement, vizElement);
  }, []);

  return (
    <div
      className="tableauPlaceholder"
      id="viz1762368155888"
      style={{ position: "relative" }}
      dangerouslySetInnerHTML={{
        __html: `
          <object class='tableauViz' style='display:none;'>
            <param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' />
            <param name='embed_code_version' value='3' /> 
            <param name='site_root' value='' />
            <param name='name' value='NFLPlaybyPlayDashboard/Sheet1' />
            <param name='tabs' value='no' />
            <param name='toolbar' value='yes' />
            <param name='static_image' value='https://public.tableau.com/static/images/NF/NFLPlaybyPlayDashboard/Sheet1/1.png' />
            <param name='display_static_image' value='yes' />
            <param name='animate_transition' value='yes' />
            <param name='display_spinner' value='yes' />
            <param name='display_overlay' value='yes' />
            <param name='display_count' value='yes' />
            <param name='language' value='en-US' />
            <param name='filter' value='publish=yes' />
          </object>
        `,
      }}
    />
  );
}
