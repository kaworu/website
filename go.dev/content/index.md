---
title: go.dev
---

<section class="Hero bluebg">
  <div class="Hero-gridContainer">
    <div class="Hero-blurb">
      <h1>Build fast, reliable, and efficient software at scale</h1>
      <ul class="Hero-blurbList">
        <li>
          <svg width="12" height="10" viewBox="0 0 12 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M10.8519 0.52594L3.89189 7.10404L1.14811 4.51081L0 5.59592L3.89189 9.27426L12 1.61105L10.8519 0.52594Z" fill="white" fill-opacity="0.87">
          </svg>
          Go is an open source programming language supported by Google
        </li>
        <li>
          <svg width="12" height="10" viewBox="0 0 12 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M10.8519 0.52594L3.89189 7.10404L1.14811 4.51081L0 5.59592L3.89189 9.27426L12 1.61105L10.8519 0.52594Z" fill="white" fill-opacity="0.87">
          </svg>
          Easy to learn and get started with
        </li>
        <li>
          <svg width="12" height="10" viewBox="0 0 12 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M10.8519 0.52594L3.89189 7.10404L1.14811 4.51081L0 5.59592L3.89189 9.27426L12 1.61105L10.8519 0.52594Z" fill="white" fill-opacity="0.87">
          </svg>
          Built-in concurrency and a robust standard library
        </li>
        <li>
          <svg width="12" height="10" viewBox="0 0 12 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M10.8519 0.52594L3.89189 7.10404L1.14811 4.51081L0 5.59592L3.89189 9.27426L12 1.61105L10.8519 0.52594Z" fill="white" fill-opacity="0.87">
          </svg>
          Growing ecosystem of partners, communities, and tools
        </li>
      </ul>
    </div>
    <div class="Hero-actions">
      <div
        data-version="{{data.global.latestVersion}}"
        class="js-latestGoVersion">
        <a class="Primary" href="https://learn.go.dev/">Get Started</a>
        <a class="Secondary js-downloadBtn"
          href="https://golang.org/dl"
          target="_blank" rel="noopener"
          >Download
          <span
            class="js-goVersion DownloadBtn-versionNum">
          </span>
        </a>
      </div>
      <div class="Hero-footnote">
        <p>
          Download packages for
          <a class="js-downloadWin">Windows 64-bit</a>,
          <a class="js-downloadMac">macOS</a>,
          <a class="js-downloadLinux">Linux</a>, and
          <a href="https://golang.org/dl/">more</a>
        </p>
        <p>
          The <code>go</code> command by default downloads and authenticates
          modules using the Go module mirror and Go checksum database run by
          Google. <a href="https://golang.org/dl">Learn more.</a>
        </p>
      </div>
    </div>
    <div class="Hero-gopher">
      <img class="Hero-gopherLadder" src="/images/gophers/ladder.svg" alt="Go Gopher climbing a ladder.">
    </div>
  </div>
</section>
<section class="WhoUses">
  {{$solutions := index (where .Pages "Section" "solutions") 0}}
  <div class="WhoUses-gridContainer">
    <div class="WhoUses-header">
      <h2 class="WhoUses-headerH2">Companies using Go</h2>
      <p class="WhoUses-subheader">Organizations in every industry use Go to power their software and services
        <a href="/solutions" class="WhoUsesCaseStudyList-seeAll">
        View all stories
       </a>
     </p>
    </div>
  <div class="WhoUsesCaseStudyList">
    <ul class="WhoUsesCaseStudyList-gridContainer">
    {{range where $solutions.Pages "Params.series" "Case Studies"}}
      {{if .Params.link }}
        {{if .Params.inLandingPageGrid }}
          <li class="WhoUsesCaseStudyList-caseStudy">
            {{$logo := .Resources.GetMatch "logo"}}
            <a href="{{.Params.link}}" target="_blank" rel="noopener"
              class="WhoUsesCaseStudyList-caseStudyLink">
              <img
                loading="lazy"
                height="48"
                width="30%"
                src="/images/logos/{{.Params.logoSrc}}"
                class="WhoUsesCaseStudyList-logo"
                alt="">
            </a>
          </li>
        {{end}}
      {{else}}
        <li class="WhoUsesCaseStudyList-caseStudy">
          <a href="{{.RelPermalink}}" class="WhoUsesCaseStudyList-caseStudyLink">
            <img
              loading="lazy"
              height="48"
              width="30%"
              src="/images/logos/{{.Params.logoSrc}}"
              class="WhoUsesCaseStudyList-logo"
              alt="">
            <p>View case study</p>
          </a>
        </li>
      {{end}}
    {{end}}
    </ul>
  </div>
</section>
<section class="TestimonialsGo">
  <div class="GoCarousel">
    <div class="GoCarousel-controlsContainer">
      <div class="GoCarousel-wrapper">
        <ul class="js-testimonialsGoQuotes TestimonialsGo-quotes">
          {{ range $index, $element := data.testimonials.all }}
            <li class="TestimonialsGo-quoteGroup GoCarousel-slide" id="quote_slide{{$index}}">
              <div class="TestimonialsGo-quoteSingleItem">
                <div class="TestimonialsGo-quoteSection">
                  <p class="TestimonialsGo-quote">{{.quote | safeHTML}}</p>
                  <div class="TestimonialsGo-author">— {{.name}},
                    <span class="NoWrapSpan">{{.title}}</span>
                    <span class="NoWrapSpan"> at {{.company}}</span>
                  </div>
                </div>
              </div>
            </li>
          {{end}}
        </ul>
      </div>
    <button class="js-testimonialsPrev GoCarousel-controlPrev" hidden>
      <i class="GoCarousel-icon material-icons">navigate_before</i>
    </button>
    <button class="js-testimonialsNext GoCarousel-controlNext">
      <i class="GoCarousel-icon material-icons">navigate_next</i>
    </button>
  </div>
  </div>
</section>

<section class="WhyGo">
  <div class="WhyGo-gridContainer">
    <div class="WhyGo-header">
      <h2 class="WhyGo-headerH2">What’s possible with Go</h2>
      <h4 class="WhyGo-headerH4">
        Use Go for a variety of software development purposes
      </h4>
    </div>
    <ul class="WhyGo-reasons">
      {{ range first 4 data.resources.resources }}
        <li class="WhyGo-reason">
          <div class="WhyGo-reasonDetails">
            <div class="WhyGo-reasonIcon" role="presentation">
              <img src="{{.icon}}" alt="{{.iconName}}">
            </div>
            <div class="WhyGo-reasonText">
              <h3 class="WhyGo-reasonTitle">{{.title}}</h3>
              <p>
                {{.description}}
              </p>
            </div>
          </div>
          <div class="WhyGo-reasonFooter">
            <div class="WhyGo-reasonPackages">
              <div class="WhyGo-reasonPackagesHeader">
                <img src="/images/icons/package.svg" alt="Packages.">
                Popular Packages:
              </div>
              <ul class="WhyGo-reasonPackagesList">
                {{range .packages }}
                  <li class="WhyGo-reasonPackage">
                    <a href="{{.url}}" target="_blank" rel="noopener">
                      {{.title}}
                    </a>
                  </li>
                  {{end}}
              </ul>
            </div>
            <div class="WhyGo-reasonLearnMoreLink">
              <a href="{{.link}}">Learn More <i class="material-icons WhyGo-forwardArrowIcon">arrow_forward</i></a>
            </div>
          </div>
        </li>
      {{end}}
      {{ if (gt (data.resources.resources | len) 3) }}
        <li class="WhyGo-reason">
          <div class="WhyGo-reasonShowMore">
            <div class="WhyGo-reasonShowMoreImgWrapper">
              <img
                class="WhyGo-reasonShowMoreImg"
                loading="lazy"
                height="148"
                width="229"
                src="/images/gophers/biplane.svg"
                alt="Go Gopher is skateboarding.">
            </div>
            <div class="WhyGo-reasonShowMoreLink">
              <a href="/solutions/#use-cases">More use cases <i
              class="material-icons
              WhyGo-forwardArrowIcon">arrow_forward</i></a>
            </div>
          </div>
        </li>
      {{end}}
    </ul>
  </div>
</section>
<section class="LearnGo">
  <div class="GoCarousel" id="LearnGo-carousel">
    <div class="GoCarousel-controlsContainer">
      <div class="GoCarousel-eventsWrapper">
        <ul class="js-goCarouselEventsSlides GoCarousel-eventsSlides">
          {{ range $index, $element := data.events.all }}
            <li
            class="GoCarousel-eventGroup"
            id="event_slide{{$index}}">
              <div class="GoCarousel-eventThumbnail">
                {{if .thumbnailurl}}
                  <img
                    loading="lazy"
                    src="{{.thumbnailurl}}"
                    alt="{{.name}} group photo">
                {{else}}
                  <img
                    loading="lazy"
                    src="/images/meetup.svg"
                    alt="meetup logo">
                {{end}}
              </div>
              <div class="GoCarousel-eventBody">
                <div class="GoCarousel-eventText">
                  <div class="GoCarousel-eventHeader">Upcoming Events</div>
                  <h4 class="GoCarousel-eventName">
                    <a href="{{.url}}">{{.name}}</a>
                  </h4>
                  <div class="GoCarousel-eventDate">
                    <p>{{.local_date}} | {{.city}}, {{.state}} {{.country}}</p>
                  </div>
                  <p class="GoCarousel-viewMore"><a href="{{.url}}">Learn more</a></p>
                </div>
              </div>
            </li>
          {{end}}
        </ul>
      </div>
      <button class="js-eventsCarouselPrev GoCarousel-controlPrev" hidden>
        <i class="GoCarousel-icon material-icons">navigate_before</i>
      </button>
      <button class="js-eventsCarouselNext GoCarousel-controlNext">
        <i class="GoCarousel-icon material-icons">navigate_next</i>
      </button>
    </div>
  </div>
</section>
<section class="GettingStartedGo">
  <div class="GettingStartedGo-gridContainer">
    <div class="GettingStartedGo-header">
      <h2 class="GettingStartedGo-headerH2">Get started with Go</h2>
      <p class="GettingStartedGo-headerDesc">
        Explore a wealth of learning resources, including guided journeys, courses, books, and more.
      </p>
      <div class="GettingStartedGo-ctas">
        <a class="GettingStartedGo-primaryCta" href="http://learn.go.dev">Get Started</a>
        <a href="https://golang.org/dl" target="_blank" rel="noopener">Download Go</a>
      </div>
    </div>
    <div class="GettingStartedGo-resourcesSection">
      <ul class="GettingStartedGo-resourcesList">
        <li class="GettingStartedGo-resourcesHeader">
          Resources to start on your own
        </li>
        <li class="GettingStartedGo-resourceItem">
          <a href="/learn#guided-learning-journeys" class="GettingStartedGo-resourceItemTitle">
            Guided learning journeys
          </a>
          <div class="GettingStartedGo-resourceItemDescription">
            Step-by-step tutorials to get your feet wet
          </div>
        </li>
        <li class="GettingStartedGo-resourceItem">
          <a href="/learn#online-learning" class="GettingStartedGo-resourceItemTitle">
            Online learning
          </a>
          <div class="GettingStartedGo-resourceItemDescription">
            Browse resources and learn at your own pace
          </div>
        </li>
        <li class="GettingStartedGo-resourceItem">
          <a href="/learn#featured-books" class="GettingStartedGo-resourceItemTitle">
            Featured books
          </a>
          <div class="GettingStartedGo-resourceItemDescription">
            Read through structured chapters and theories
          </div>
        </li>
        <li class="GettingStartedGo-resourceItem">
          <a href="/learn#self-paced-labs" class="GettingStartedGo-resourceItemTitle">
            Cloud Self-paced labs
          </a>
          <div class="GettingStartedGo-resourceItemDescription">
            Jump in to deploying Go apps on GCP
          </div>
        </li>
      </ul>
      <ul class="GettingStartedGo-resourcesList">
        <li class="GettingStartedGo-resourcesHeader">
          In-Person Trainings
        </li>
        {{range first 4 data.learn.inPerson.links }}
          <li class="GettingStartedGo-resourceItem">
            <a href="{{.url}}" class="GettingStartedGo-resourceItemTitle">
              {{.title}}
            </a>
            <div class="GettingStartedGo-resourceItemDescription">
              {{.blurb}}
            </div>
          </li>
        {{end}}
      </ul>
    </div>
  </div>
</section>