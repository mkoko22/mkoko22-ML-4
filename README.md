Assignment 4

პროექტი მიზნად ისახავს ფოტოსურათებიდან სახის ემოციების ამოცნობას, კერძოდ წარმოადგენს kaggle - ის შეჯიბრს Challenges in Representation Learning, Facial Expression Recognition Challenge.
დასაწყისისთვის გავაკეთე ყველაზე მარტივი CNN, სადაც იყო ორი კონვოლუციური და ორი სრულად დაკავშირებული ფენა. ამ მოდელმა გამოავლინა საფუძვლიანი შედეგები, თუმცა იყო სივრცე გაუმჯობესებისთვის. ამის შემდეგ დავამატე Batch Normalization ფენები, რომელიც ეხმარება მოდელს უფრო სწრაფად და სტაბილურად სწავლაში და ასევე ამცირებს overfitting-ის ალბათობას. 
რამდენჯერმე პარამეტრებისას არასწორი რეგულაციისას, ეპოქების რაოდენობის თუ learning rate-ს გამო, მივიღე ძალიან overfitted შედეგი (~75% train, ~50% test). თუმცა ცვლილებებმა გამოიღო შედეგი და ისინი ერთმანეთს დაუახლოვდა. შემდეგ ეტაპზე გამოვიყენე Dropout ფენები, როგორც კონვოლუციურ, ასევე Fully Connected ნაწილში, რათა კიდევ უფრო შემცირებულიყო მოდელის overfitting. თითოეულ ეტაპზე ვიყენებდი სხვადასხვა მონაცემთა აეუგმენტაციას, 'როტაციას', რაც ამდიდრებდა მოდელის შემეცნებით შესაძლებლობებს და ამცირებდა მოდელის მიერ სიმეტრიულ ან კონკრეტულ მაგალითებზე დამოკიდებულებას.

ტრენინგის პროცესში რეგულარულად ვაკვირდებოდი train და validation loss-ს და accuracy-ს, რასაც Wandb პლატფორმაზე ვლოგავდი, თუმცა ძალიან ბევრი ლოგის დაგროვების გამო, საბოლოოდ ზედმეტი ლოგებისგან გავათავისუფლე და ბოლოდროინდელი ტრეინის შედეგები დავტოვე. 

ყველა ექსპერიმენტი მიმდინარეობდა Google Colab-ის გარემოში.

ჩემი მიდგომა იყო ექსპერიმენტული, პატარა არქიტექტურიდან დაწყება და ეტაპობრივად სხვადასხვა ტექნიკის გატესტვა: BatchNorm, Dropout, Data Augmentation და სწავლების პარამეტრების (ლერნინგ რეითი, ბაჩ საიზი, ეპოქები) ცვლილება.

მადლობა.
