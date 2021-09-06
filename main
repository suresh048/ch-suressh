public class Main 
{
    public static void main(String[] args) 
    {
        CustomerOne s1 = new CustomerOne();
        CustomerTwo s2 = new CustomerTwo();
        CustomerThree s3 = new CustomerThree();
		//synchronization is used to make sure any observer registered after message is
		//received is not notified
         
        MerchandisePublisher p = new MerchandisePublisher();
         
        p.attach(s1);
        p.attach(s2);
        //s1 and s2 will receive the update
        p.notifyUpdate(new Merchandise("We have new merch"));  
         
        p.detach(s1);// s1 is removed and only s2 and s3 remain
        p.attach(s3);
         //s2 and s3 will receive the update
        p.notifyUpdate(new Merchandise("New merch has arrived !!!")); 
    }
}
