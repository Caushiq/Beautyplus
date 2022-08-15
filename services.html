<?php
include("includes/connection.php");
$query_cat_id=$_GET['category_id'];
$id_arr=$_GET['id_arr'];
$id_arr=explode(",",$id_arr);
?>
<!DOCTYPE html>
<html>
	<head>
		<?php include("includes/header_include_files.php"); ?>
        <title>
        <?php
        $sel=mysqli_query($link,"select * from `category_master` where `id`='".$query_cat_id."' order by `id` ASC");
        $arr=mysqli_fetch_array($sel);
        $category_name=$arr['name'];
        echo $category_name; 
        ?>
        </title> 
	</head>
	<body>
		<?php include('includes/header.php');?>
        <br><br><br><br><br>
        <div class="container">
	        <div class="d-flex mt-0 mr-1" id="servicediv">
				<?php
				$sel=mysqli_query($link,"select * from `category_master` where `status`='1' order by `id` ASC");
				while($arr=mysqli_fetch_array($sel))
				{
					$category_id=$arr['id'];
					$category_name=$arr['name'];
					?>
					<a style="text-align: center;" href="#" class="primarybtn" id="<?php if($query_cat_id==$category_id){echo 'category_div';}?>" onclick=setUrl("<?php echo $category_id; ?>");><?php echo $category_name; ?></a> 
					<?php
				}
				?>
	        </div>
    	</div>
		<div class="container">
			<?php
			$category_id=$_GET['category_id'];
			$select=mysqli_query($link,"select * from `service_master` where `cat_id`='".$category_id."' and `status`='1'");
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
			?>
		
			<div class="ml-0 mt-1 mr-0 mb-1" id="itemdiv">
				<div class="itemdiv">
					<img id=imgproduct src="admin/images/<?php echo $imgName; ?>.jpg" alt="">
					<div style="margin-top: 10px; max-width: 56%; width: 56%;">
						<h6 id="productname"><?php echo $name; ?></h6>
						<h6 id="prodprice"><i id="validprice" class="fa fa-inr" aria-hidden="true"></i> <?php echo $discounted_price; ?> <s><i id="oldprice" class="fa fa-inr" aria-hidden="true"></i><?php echo $total_price; ?></s></h6>
						<div style="font-size: 13px; font-weight: 500; margin-left: 10px; margin-top: 5px; color: rgb(70, 69, 69);">
							<i style="font-size: 13px;color: rgb(70, 69, 69);" class="fa fa-clock-o" aria-hidden="true"></i>&nbsp; <?php echo $timing; ?> Min
						</div>
						<div>
							<i style="color:#808080">Code - <?php echo $package_code; ?></i>
						</div>
					</div>
					<div class="product-action-2" id="add_button_div_<?php echo $service_id; ?>">
						<?php
						if(in_array($service_id, $id_arr))
						{
							?>
							<input class="mt-5 " type="button" id="additem" value="Remove" class="btnAddAction btn" onclick="removeCart('<?php echo $service_id; ?>', '<?php echo $name; ?>');"/>
							<?php
						}
						else
						{
							?>
							<input class="mt-5 " type="button" id="additem" value="ADD +" class="btnAddAction btn" onclick="addCart('<?php echo $service_id; ?>', '<?php echo $name; ?>');"/>
							<?php
						}
						?>
						
					</div>
				</div>
				<div class="p-1 " style="margin-left: 5px; margin-top: 2px;">
					<h5 style="font-size: 13px;">Package Desciption :</h5>
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
				<div class="ml-2 mb-3">
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
		  ?>
		</div>
		
		<div class="float-left">
		</div>
		<?php include('includes/footer.php');?>
        <?php include('includes/footer_include_files.php');?>
	</body>
</html>