# Pet Salon Transactions

I explored a Pet Salon database named dog_salon with a transactions table that is a snapshot of some of the transactions that occurred in the week of 6/16/19 to 6/22/19. 

Fields include the following:
<br>transaction_id (integer)
<br>date (date)
<br>pet_id (integer)
<br>service (string)

The owners table includes the following fields:
<br>owner_id (integer)
<br>pet_id (integer)
<br>size (string), size of pet

The owners_2 table lists additional owners including some of the same owners who appear in owners who may own more than one dog. 
<br>Fields include the following:
<br>owner_id (integer)
<br>pet_id (integer)
<br>size (string), size of pet

The visits table includes the following fields:
<br>pet_id (integer)
<br>visits_count (integer)

## #1
Write a query that returns the owner_id of the owners table and the transaction_id and service of the transactions table.
Ensure that all records from the transactions table are returned, and sort the results in ascending order according to owner_id.

<img width="531" alt="1" src="https://github.com/romaoeh/PetSalon/assets/131217181/62ec4bd6-7350-4a2f-8e38-a8f6ac641355">
<img width="531" alt="1 5" src="https://github.com/romaoeh/PetSalon/assets/131217181/c01bdf15-e3bf-421c-b91c-bb6edd3a0890">

## #2
Write a query that returns the owner_id, pet_id, transaction_id, and visits_count fields from their respective tables. Sort in order of transaction_id.
Do not include records where transaction_id is NULL.

<img width="536" alt="2" src="https://github.com/romaoeh/PetSalon/assets/131217181/dec31ee4-c5f5-48bd-9163-be0b628e027a">
<img width="536" alt="2 5" src="https://github.com/romaoeh/PetSalon/assets/131217181/4f24a5aa-7423-4aa2-88c2-45b8ed01fb9c">

## #3
Write a query that returns the pet_id and size from the owners table, and the visits_count (as the alias num_visits) from the visits table.
Keep only the records where dogs had 10 or more visits, and sort by the number of visits in descending order.

<img width="547" alt="3" src="https://github.com/romaoeh/PetSalon/assets/131217181/caf0d637-14e2-4f65-8fce-15449af9eac7">
<img width="547" alt="3 5" src="https://github.com/romaoeh/PetSalon/assets/131217181/3951b038-75ed-42f9-80db-ab50c965c60f">

## #4
There are 2 tables, owners and owners_2, that have information about dog owners. You want the list of all unique dog owners from both tables.
Combine these 2 tables and return a single field that shows a list of owner_id records from both input tables, and order by owner_id. Keep only unique records.

<img width="570" alt="4" src="https://github.com/romaoeh/PetSalon/assets/131217181/aa7caed7-49a5-48c4-9e0e-0adbd99d530b">

## #5
You're having a customer rewards promotion, and you want to identify your top three customers (owner_id) based upon how many visits they've had.
You also know that some owners have more than one pet, so you want to add up all of their visits across all pets. Once you have this, select the top three customers (owner_id) and list them in descending order according to number of visits (using the alias num_visits)!

<img width="547" alt="5" src="https://github.com/romaoeh/PetSalon/assets/131217181/dfff298a-2ad4-4149-97d1-77550120e9b7">
<img width="547" alt="5 5" src="https://github.com/romaoeh/PetSalon/assets/131217181/2633d077-e682-4af9-8d1f-3c06d6936072">

## #6
Write a query that returns owner_id from both the owners and owners_2 tables and include the transaction_id, date, and service fields from the transactions table. Sort your results first by date, then by transaction_id, and finally by owner_id in descending order. All rows from owners and owners_2 tables should be returned. Do not include records where transaction_id is NULL.

<img width="547" alt="6" src="https://github.com/romaoeh/PetSalon/assets/131217181/a8597ebc-28ec-4336-b773-fef7f523e6e4">
<img width="547" alt="6 5" src="https://github.com/romaoeh/PetSalon/assets/131217181/d2743e76-069a-448c-8dbd-979301ff6aa1">

## #7
Return a table that includes all records from both owners and owners_2 tables, and include a new field, owner_pet which is formatted as owner_id, pet_id (in other words, the owner ID followed by a comma, then a space, then the pet ID).

Return only the rows where the number of visits is greater than or equal to 3. Sort the results by number of visits (largest to smallest), and if there's a tie in this number, sort by your newly created owner_petfield.

Use the CONCAT() function for this operation instead of the concat operator (||), as they behave differently when working with NULL values.
You may notice that the same pet is owned by two different owners. Although uncommon, this is not necessarily an error.

<img width="539" alt="7" src="https://github.com/romaoeh/PetSalon/assets/131217181/4a28b0f6-c05a-48e2-a519-7c3ea296b650">
<img width="539" alt="7 5" src="https://github.com/romaoeh/PetSalon/assets/131217181/76cc03c6-7245-49ce-98ff-4d77889d9dd9">

## #8
Show the visit counts for each pet, and order the output from most to least visits. Include the owner_id, pet_id, and visits_count columns in your output.

<img width="502" alt="8" src="https://github.com/romaoeh/PetSalon/assets/131217181/e4d07851-2463-46c1-ba6d-59f373121d17">
<img width="502" alt="8 5" src="https://github.com/romaoeh/PetSalon/assets/131217181/7bd0f812-f499-443d-8197-e816afcac653">

## #9
Write a query that returns the owner_id, pet_id, date, and service for transactions that happened on June 17th, 2019, or for transactions where the service provided was a haircut. Order your results by date.

<img width="499" alt="9" src="https://github.com/romaoeh/PetSalon/assets/131217181/8a65d6bd-c0a4-496a-9da6-ec0c2ae1133c">
<img width="499" alt="9 5" src="https://github.com/romaoeh/PetSalon/assets/131217181/bf0cd087-61d8-4140-b948-9b6b27e6bcc4">

## #10
You have a promotion where you'd like to give a gift to those pets who have had their nails done at the salon.
Write a query that shows the pet_id and service for those pets that used the nails service from transactions. Then sort by those pets first who are receiving a gift.

Use a CASEstatement that assigns gift when the service is nails, and otherwise assigns no gift. End your CASE statement with the alias get_gift, and order by this field.

<img width="502" alt="10" src="https://github.com/romaoeh/PetSalon/assets/131217181/d8010d0d-a9b9-43a9-b35c-0f68769f8ebd">
<img width="502" alt="10 5" src="https://github.com/romaoeh/PetSalon/assets/131217181/5275cc33-2385-48f5-9692-18e3f54c22b4">


