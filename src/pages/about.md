---
layout: ../layouts/AboutLayout.astro
title: "About"
description: "About me"
---

<!--suppress HtmlUnknownTarget -->
<div>
  <!--suppress HtmlUnknownTarget -->
    <img src="/assets/avatar.jpeg" class="mx-auto w-48 h-48 rounded-full object-cover" alt="coding dev illustration">
</div>
<p class="text-center">
    Hi, I'm flyingcrp(Chen Shiyi), born in 1991
</p>
<p class="text-center">
    <span id="my_date"></span>
</p>
<p class="text-center">
    <span id="year"></span>
</p>

## Journey

<p class="font-bold italic">Career trajectory</p>

- 07/2022 ~ present (CTO)
- 05/2018 ~ 05/2022 (CO-Founder & CTO)
- 09/2015 ~ 03/2018 (Full Stack Developer)
- 10/2014 ~ 08/2015 (Frontend Developer)
- 09/2011 ~ 07/2014 (Backend Developer)

<script>
function getAge() {
    const specifiedDate = new Date("2011-09-01");
        const currentDate = new Date();
        let yearDiff = currentDate.getFullYear() - specifiedDate.getFullYear();
        let month = currentDate.getMonth();let monthDiff = month - specifiedDate.getMonth();
        if (monthDiff < 0) {
            yearDiff--;
            monthDiff += 12;
        }
        const currentDateElement = document.getElementById("year");
        currentDateElement.innerText = `${yearDiff} years and ${monthDiff} months of work experience`;
        const myDate=document.getElementById("my_date");
        month=month+1;
        myDate.innerText=`09/2011 ~ ${month>9?month:`0${month}`}/${currentDate.getFullYear()}`;
    }
    getAge()
</script>
