# k8sIntro

creating secrets:

`kubectl create secret generic twilio-secret --from-literal TWILIO_ACCOUNT_SID="AC2d698b700eca92aeba0cd40782912052" --from-literal TWILIO_AUTH_TOKEN="b0e3c5292a4ea895afb4417ec16f1738" --from-literal TWILIO_NUMBER="+18334893511"
    `


updating image for prod deployment in k8s cluster:
`kubectl set image deployment/store store=edwardkemper/store-app:v2`


here are the steps that the CD pipeline will take:
* login to aws for access to the k8s cluster
* login to docker hub to get and push images
* build image
* push image to docker hub
* install kubectl
* set kubectl context
* set the deployment image
* re- apply the deployment confi in the EKS context


# some data for testing



{
  "product": {
      "image": "https://www.rebootwithjoe.com/wp-content/uploads/2013/06/Almond-Butter-Chocolate-Fudge.jpg",
      "price": 14.33,
      "description": "Gooey and creamy chocolate",
      "_id": "62c5fee277de00fe92c75f27",
      "__v": 0
  }
}
{
    "name": "Red Velvet",
    "image": "https://media.istockphoto.com/photos/red-velvet-cake-picture-id485832764?k=20&m=485832764&s=612x612&w=0&h=58yxSE0lOx3aD7OZJ3wodakdAbEB-aH6MWNj3QGutwg=",
    "description": "Moist with cream cheese icing",
    "price": 34.33
},
{
    "name": "Raspberry Cheesecake",
    "image": "https://www.elmundoeats.com/wp-content/uploads/2020/06/FP-No-Bake-Raspberry-Cheesecake.jpg",
    "description": "New York style cheesecake",
    "price": 64.33
}
