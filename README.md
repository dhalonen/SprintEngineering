# A Reflection on Sprint Engineering
Sprint stories are designed to deliver short term results that must be integrated into a whole over time. There are costs that should be considered, as no single tool or process is without costs.

Sprint engineering is the effort to extract from a bigger feature a smaller piece of work as to fit within a sprint. So what comprises that effort? 

1. Resources must be expended to plan the piecemeal work: what can be broken out, how will it be tested, when each piece be developed, when does it get put back together, what testing coordination is required on the assembly, ... For any complex problem, this is a significant amount of planning not only by the leads, but during team planning meetings and retrospectives. In other words, typically leads may do the initial piece breakout and then spend total team time communicating the effort.

1. There can be a significant time lapse between the initial piecemeal planning and the start of work. Even if the whole team is involved with the piecemeal planning, that understanding & context is likely long gone when work commences. That developer must the re-constitute that understanding and if the stars align, that developer was a part of the initial planning. The initial estimate of work assurdly doesn't include the developer & tester's time to rebuild that initial context.

1. A piecemeal solution may require resoures that the full solution provides. For example, the piecemeal solution may need to perform a database lookup that the main feature already has in place. Or alternatively, by the time the pieces are pulled together, the main feature has the data in hand and the piecemeal feature will either re-query or that query must be removed. In other words, the piecemeal solution demands built-in waste.

1. The piecemeal waste is increased when considering testing as those test cases must also be rolled into the bigger feature. It's even worse if the practice demands automated tests on the piecemeal feature. Who has the forsight to remove irrelevant automated tests? What if the test count must remain monotonically increasing? This introduces the need for additional engineering to support the piecemeal test, while not incuring the waste in the main feature.

2. The plans to merge the piecemeal into the whole likely are hopelessly optimistic. After all the work done by disparate develoeprs over several sprints demonstrates delivered value! All that remains is to simply stitch these efforts together. What can possibly go wrong?

## Is there a better way?
Yes. If one understands the above risks, then they would be prepared to consider the costs or examine alternatives. Directly dealing with the costs is simply doing deeper dives & analysis to catalog the problems and then work to mitigate. In other words, added cost.

There is a notion that features should be delivered in slices from top-to-bottom. This has proven to be effective in some examples, such as shopping cart websites. If the problem domain is more complex, say to deliver a radiology imaging solution with a database analysis tool, the "slice" approach may not be so great.

An alternative approach would be to use a "tracer bullet" approach (https://pragprog.com/tips/ is a great read from 20 years ago, as well as the updated edition.) With this approach, a skeleton system from the imaging machine to the image storage system, to the database, to the rendering and reporting software is developed. Likely, it would deliver a "Hello World" image and expose many, many issues along the way. From there features can be built on with less waste.

## Is your situation unique?
Of course, but who cares? Step back and consider the waste your practice may be implementing. It may not be practical or even desireable to eliminate all waste, so don't be dogmatic.

