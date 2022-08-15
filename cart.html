<?php
include("includes/mail.php");
include("includes/connection.php");
$id_arr=$_GET['id_arr'];
if(isset($_POST['submit']))
{
		$client_name=mysqli_real_escape_string($link,$_POST['client_name']);
		$schedule_date=mysqli_real_escape_string($link,$_POST['schedule_date']);
		$mobile=mysqli_real_escape_string($link,$_POST['mobile']);
		
		$name_reg='/^[a-zA-Z\.  ]{2,100}$/';
		$mobile_reg='/^[0-9]{10}$/';
		$date_reg='/^[0-9]{2}[\-]{1}[0-9]{2}[\-]{1}[0-9]{4}$/';

		if(!preg_match($name_reg,$client_name))
		{
			$msg="<span id='error'>Please Enter correct Name</span>";
		}
		else if(!preg_match($date_reg,$schedule_date))
		{
			$msg="<span id='error'>Please enter correct date format(DD-MM-YYYY)</span>";
		}
		else if(!preg_match($mobile_reg,$mobile))
		{
			$msg="<span id='error'>Please enter correct Mobile Number.</span>";
		}
		else
		{
			$schedule_date=dbFormat($schedule_date);
			mysqli_query($link,"INSERT INTO `schedule_master`(`client_name`, `schedule_date`, `mobile`, `service_id`, `added_date`) VALUES ('".$client_name."', '".$schedule_date."', '".$mobile."', '".$id_arr."', '".date('Y-m-d H:i:s')."')");
			$email="nastech9891@gmail.com";
			$to=$email;
    	$mail->IsHTML(true);
      $mail->AddAddress($to, "Query Email");
      $mail->SetFrom("from-nastech9891@gmail.com", "Beauty Pluses No Reply Email");
      $mail->Subject = "New Query";

      $id_arr=explode(",",$id_arr);
      $services_selected="";
        $total_price=0;
      foreach($id_arr as $key=>$val)
      {
      	$select=mysqli_query($link,"select *, (select name from category_master where category_master.id=service_master.cat_id limit 1) as 'cat_name' from `service_master` where `id`='".$val."'");
      	$array=mysqli_fetch_array($select);
      	$services_selected="<p><b>Name : </b>".$array['cat_name']."<br><b>Service : </b>".$array['name']."<br><b>Code : </b>".$array['package_code']."<br><b>Service Description : </b>".$array['service_description']."<br><b>Discounted Price : </b> Rs.".$array['discounted_price']."</p><br>".$services_selected;
          $total_price=$total_price+$array['discounted_price'];
      }
            
      $schedule_date=dbFormat($schedule_date);

      $content = "<table width='100%' border='1'><tbody><tr><th>Client Name</th><td>".$client_name."</td></tr><tr><th>Mobile</th><td>".$mobile."</td></tr><tr><th>Schedule Date</th><td>".$schedule_date."</td></tr><tr><th>Total Discounted Price</th><td>Rs. ".$total_price."</td></tr><tr><th>Services Description</th><td>".$services_selected."</td></tr></tbody></table>";
      
      $mail->MsgHTML($content);
      if(!$mail->Send())
      {
          $msg="<span id='error'>Email Sending Error</span>";
      } 
      else 
      {
      	?>
      	<script>alert("Your services has been scheduled successfully"); window.location.href="index.php"</script>
      	<?php
      }
		}
}
?>
<!DOCTYPE html>
<html>
	<head>
		<?php include("includes/header_include_files.php"); ?>
    <title>Cart</title> 
	</head>
	<body>
    <form method="post">
		<?php include('includes/header.php');?>
    <br><br><br><br>
		<div class="container">
			<center><p><?php echo $msg; ?></p></center>
			<?php
      $service_list_id=explode(",",$id_arr);
      foreach($service_list_id as $key_service=>$val_service)
      {
			$select=mysqli_query($link,"select *, (select name from category_master where category_master.id=service_master.cat_id limit 1) as 'cat_name' from `service_master` where `id`='".$val_service."' and `status`='1'");
			while($array=mysqli_fetch_array($select))
			{
            $service_id=$array['id'];
			$name=$array['name'];
			$discounted_price=$array['discounted_price'];
			$total_price=$array['total_price'];
			$timing=$array['timing'];
			$package_code=$array['package_code'];
			$service_description=$array['service_description'];
			$free_service=$array['free_service'];
            $imgName=$array['img_name'];
            $catName=$array['cat_name'];
            $category_id=$array['cat_id'];
            $discount_percent=round($discounted_price/$total_price*100,0)
			?>
			<div class="ml-0 mt-1 mr-0 mb-1" id="itemdiv">
				<div class="itemdiv">
					<img id=imgproduct src="admin/images/<?php echo $imgName; ?>.jpg" alt="">
					<div style="margin-top: 10px; max-width: 56%; width: 56%;">
                        <a style="text-align: center;" class="primarybtn" id="category_div" onclick=setUrl("<?php echo $category_id; ?>");><?php echo $catName; ?> &#10004;</a>
						<h6 id="productname"><?php echo $name; ?></h6>
						<div style="float: right; margin-top:-5%; margin-right:1%;">
                            <h6 id="validprice" class="bg-success text-white" ><?php echo $discount_percent ?>% Discounted</h6>
                        <h6 id="prodprice"><i id="validprice" class="fa fa-inr" aria-hidden="true"></i><?php echo $discounted_price; ?> 
<!--                            <s><i id="oldprice" class="fa fa-inr" aria-hidden="true"></i><?php echo $total_price; ?></s>-->
                        </h6>
                        </div>
<!--
						<div style="font-size: 13px; font-weight: 500; margin-left: 10px; margin-top: 5px; color: rgb(70, 69, 69);">
							<i style="font-size: 13px;color: rgb(70, 69, 69);" class="fa fa-clock-o" aria-hidden="true"></i>&nbsp; <?php echo $timing; ?> Min
						</div>
-->
						<div>
							<i style="color:#808080">Code - <?php echo $package_code; ?></i>
						</div>
					</div>
					
				</div>
				<div class="p-1 " style="margin-left: 5px; margin-top: 2px;">
<!--					<h5 style="font-size: 13px;">Package Desciption :</h5>-->
					<h6 style="font-size: 13px;"><i style="color:  rgb(58, 57, 57);" class="" aria-hidden="true"></i>
						<?php 
						$service_description=explode("<br>",$service_description);
						foreach ($service_description as $key => $value) 
						{
							echo "&#10004; ".$value."<br>";
						}
						?>
					</h6>
				</div>
				<div class="">
					<?php 
                    if($free_service=="None")
                    {
                    }
                    else
                    {
                        ?>
                    <b style="color: white; background-color: #F31258; font-size: 12px; padding: 4px; border-radius:; border: margin-left:;"> FREE SERVICES</b>
					<h6 class="ml-0" style="font-size: 13px; margin-top: 10px;"><i style="color:  rgb(58, 57, 57,); margin-top: 15px;" class="" aria-hidden="true"></i>
                      <?php  
					$free_service=explode("<br>",$free_service);
					foreach ($free_service as $key => $value) 
					   {
						echo "&#10004; ".$value."<br>";
					   }
                    }
					?>
					</h6>
				</div>
			</div>
            <?php
		  }
        }
            ?>
		<input class="btn btn-primary btn-lg" type="button" value="Schedule Your Services"  style="width:100%;" data-toggle="modal" data-target="#exampleModal"/>
        <div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true" style="padding-top:8%;">
          <div class="modal-dialog" role="document">
            <div class="modal-content">
              <div class="modal-header">
                <h5 class="modal-title" id="exampleModalLabel">Schedule Your Service</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                  <span aria-hidden="true">&times;</span>
                </button>
              </div>
              <div class="modal-body">
              		<lable>Enter Your Name</lable>
                	<input type="text" name="client_name" id="client_name" required="required" class="form-control" maxlength="100" value="<?php echo $client_name; ?>"/>

              		<lable>Choose Schedule Date</lable>
                	<input type="text" name="schedule_date" id="datepicker" required="required" class="form-control" autocomplete="off" value="<?php echo $schedule_date; ?>"/>
                	<p id="error">(DD-MM-YYYY)</p>
                	
                	<lable>Enter Mobile No.</lable>
                	<input type="text" name="mobile" id="mobile" required="required" class="form-control" maxlength="10" value="<?php echo $mobile; ?>"/>
              </div>
              <div class="modal-footer">
                <button type="submit" class="btn btn-primary" name="submit">Submit</button>
              </div>
            </div>
          </div>
        </div>
        </div>
		
		<div class="float-left">
		</div>
		<?php include('includes/footer.php');?>
		<?php include('includes/footer_include_files.php');?>
    </form>
	</body>
</html>