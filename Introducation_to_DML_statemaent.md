###Apex DML (Data Manipulation Language) is a part of the Apex programming language that allows you to perform database operations in Salesforce. Apex DML enables you to insert, update, delete, and upsert records in the database. You can use Apex DML to manipulate both standard and custom objects.

Here is an example of an Apex DML statement that inserts a new account record:
Account a = new Account(Name='My Account');
insert a;

You can also use Apex DML to update existing records:
```js Account a = [SELECT Id, Name FROM Account WHERE Name='My Account'];
a.Name = 'Updated Account Name';
update a;

```

To delete a record, you can use the delete keyword:

Account a = [SELECT Id, Name FROM Account WHERE Name='Updated Account Name'];
delete a;

Finally, you can use the upsert keyword to either update an existing record or insert a new one, depending on whether a record with a matching unique field value already exists:

Account a = new Account(Name='My Account', External_Id__c='abc123');
upsert a External_Id__c;


I hope this gives you a good introduction to Apex DML! Let me know if you have any questions.
