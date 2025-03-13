**Auction System:**
This project is a real-time auction system that allows multiple users to place bids on various items simultaneously. The core functionality is built using Java multithreading to handle concurrent users, ensuring synchronized access to auction data and preventing race conditions.This system simulates a real-world online auction platform, where:
1. Users can join an auction and bid.
2. Bids are processed in real-time.
3. The auction automatically ends after a set time.
4. Proper synchronization ensures that bids are handled fairly without conflicts.

***Core Features:***
✅ User Registration & Login ===> Users should be able to sign up and authenticate.
✅ Auction Creation ==> Sellers can create new auctions for items.
✅ Real-time Bidding ==> Multiple users can place bids simultaneously.
✅ Multithreaded Bid Processing ==> Ensures no two users can bid at the exact same time without synchronization.
✅ Auction Closing Mechanism ==> The auction automatically ends after a defined period.
✅ Winner Announcement – Declares the highest bidder as the winner.

**Implement Core Classes:**
1. User Class
      Represents buyers & sellers in the system.
      Attributes: userID, username, bidsPlaced
2. AuctionItem Class
      Represents an item being auctioned.
      Attributes: itemID, itemName, basePrice, highestBid, currentWinner, endTime.
3. Bid Class
      Represents a bid made by a user.
      Attributes: bidID, amount, bidder, timestamp.
4. AuctionManager Class (Handles Threading)
      Starts auctions.
      Manages concurrent bidding using synchronized methods.
      Closes auctions after a timeout.
5. Multi-threading Mechanism
      Uses ExecutorService to manage multiple bidding threads.
      Synchronizes bid updates.

**Implement Multi-threaded Bid Processing:**
1. Each user runs in a separate Thread.
2. Bidding happens concurrently, and the highest bid is safely updated.
3. Use synchronization (synchronized methods, locks, or atomic variables) to prevent inconsistent bids.

**Implement Auction Closing:**
1. Auction runs for a fixed duration (e.g., 60 seconds per item).
2. Uses ScheduledExecutorService to close it after the timer ends.
3. Announces the highest bidder.




