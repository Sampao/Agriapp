

from django.db import models

# Create your models here.


class Farmer(models.Model):
    farmer_name = models.CharField(max_length=20)
    farmer_information = models.CharField(max_length=100)
    location = models.CharField(max_length=1000)
    contacts = models.CharField(max_length=10)


class Product(models.Model):
    farmer = models.ForeignKey(Farmer, on_delete=models.CASCADE)
    product_type = models.CharField(max_length=100)
    product_amount = models.CharField(max_length=1000)
    selling_prize = models.CharField(max_length=3000)







