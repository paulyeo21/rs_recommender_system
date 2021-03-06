#rs_recommender_system

###Summary

This recommender is made up of three classes: Recommender, UserBasedRecommender, and ContentBasedRecommender. True to their names the UserBasedRecommender uses a user-based filtering algorithm and the ContentBasedRecommender uses a category-based filtering algorithm. The Recommender class holds basic functionality to parse data into relevant data structures. The bulk of the recommender's work is done by building a cosine similarity matrix between pairs of users and pairs of items using their associated categories.

###Set-up and Test

```ruby
# using rbenv
rbenv local 2.2.2
bundle
rbenv rehash
rspec spec/*_test.rb
```

###Recommendations

From root directory 'rs_recommender_system' run these commands

```ruby
# content-based recommender strategy
ruby lib/content_based_recommender.rb "username"
```

```ruby
# user-based recommender strategy
ruby lib/user_based_recommender.rb "username"
```

###Data

The dataset used for this was provided by Retention Science and is under the "data" directory. 

###Next

The efficiency of the recommender hinges on building the cosine similarity matrix. If the matrix is built, the recommendations come swimmingly. Further work I would try and implement algorithms that scale better such as slope one and add a k-nearest neighbor wrinkle into the similarity algorithm.
