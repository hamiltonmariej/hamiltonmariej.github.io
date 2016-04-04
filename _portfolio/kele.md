---
layout: post
title: Kele API
feature-img:
thumbnail-path:
short-description: A Ruby Gem API client to access the Bloc API.

---
## Summary
Bloc's API provides an external facing JSON Web Token authorized gateway to the Bloc application.  The Kele API Client provides easy access to and use of the student endpoints of Bloc's API.  To help facilitate that ease, Kele is built as a Ruby Gem for loading into any Rails project.  Find the project on [Github]: https://github.com/hamiltonmariej/Kele.

## Problem
There is a need for an easier way than cURL to access the Bloc Application API to incorporate into a separate application or API.  A user wants to be able to:
*Initialize and authorize Kele wih a Bloc username and password;
*Retrieve the current user as a JSON blob;
*Retrieve a list of their mentor's availability;
*Retrieve Bloc curriculum roadmaps and checkpoints; and
*Retrieve a list of their messages, respond to an existing message, and create a new message thread.

## Solution
A server side API Ruby Gem that can solve all the use cases built with Rails 4. , HTTParty, JSON, ...
An error notification was added so that the user is aware that if a call fails due to incorrect authorization credentials, they are notified and can correct the credentials.

{% highlight ruby %}
````
class InvalidStudentCodeError < StandardError
  def initialize(msg="invalid email or password")
    super(msg)
  end
end
````
{% endhighlight %}

## Results
Kele was successfully created.  My current plan is to go back and improve Kele by creating a test suite that uses Minitest and Faraday instead of RSpec and Webmock.  If time allows, I would also add a variety of error notifications for failed calls for ease of use.

## Conclusion
I really enjoyed this project and learning the differences between developing a Rails application or Rails application and API versus a Ruby Gem.  I like the simplicity of Gem development but the numerous options that gem development brings.
