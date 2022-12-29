# SOQL-DELETE-UNDELETE

// delete
List<Account> x=[SELECT Name, Id FROM Account where name like '%sirket1%'];
List<Account> z=new List<Account>();
for(Account y:x){
    if(y.name=='sirket1'){
     z.add(y) ;    }
}
delete z;*/

//undelete
List<Account> x=[SELECT Id, IsDeleted, Name FROM Account  ALL ROWS];
List<Account> z=new List<Account>();
for(Account y:x){
   
    System.debug(y.name+' '+y.isdeleted);
}undelete z;

