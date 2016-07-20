# Gannett Developer Candidate Exercise

Greetings! This exercise was written to provide developers with an opportunity to show off their mad coding chops.

If you do not understand, or are unable to complete some of the acceptance criteria in this exercise, don't panic! The exercise was written by fellow developers that are just as eager to see how you approach a problem as they are to see the end result.

## Feature Set Overview

The goal of this exercise is to deliver a single page of personalized content in an efficient, scalable manner.

### Acceptance Criteria

1. Visiting "/" on the web application server should display an HTML page.
	1. At the top of the page a headline should display with the following content: "My Delicious Articles"
	2. A profile id should be retrieved from "https://peaceful-springs-7920.herokuapp.com/profile/" on every page load.
		1. The profile id should persist the same value across requests for 365 days.
	3. Using the profile id acquired, profile specific content should be retrieved from "https://peaceful-springs-7920.herokuapp.com/content/PROFILE_ID/".
		1. The "articles" from the profile specific content should be displayed directly below the headline.
			1. The articles should be displayed in the order they were returned by the endpoint.
			2. For each item the article's "title" should appear first.
			3. For each item the article's "summary" should appear directly below its "title".
			4. For each item the "title" and "summary" should be links to that article's "href".
		2. If the profile specific content includes a "theme" with the value "rare", the HTML page's default text color should be crimson (#DC143C).
		3. If the profile specific content includes a "theme" with the value "well", the HTML page's default text color should be saddle brown (#8B4513).
2. The feature set should be delivered as a GitHub pull request against this repository's "master" branch.
	1. The pull request should include step-by-step instructions describing how the feature set can be run locally.

### Technical Notes

1. This exercise can be completed with any common web language or framework (Go, Java, Node.js, Python, Ruby, etc.). Any tool-set that can be used to fulfill the acceptance criteria is welcome.
2. The profile id endpoint referenced above automatically uses a cookie to preserve the profile id across requests.
3. Both endpoints in the acceptance criteria above support a content type of either "application/json" or "application/javascript" (JSONP). The JSONP callback query string parameter is "callback".
4. The exercise is relatively short to allow time for ample polish. Consider the implementation's: scalability, test coverage, readability, etc.
