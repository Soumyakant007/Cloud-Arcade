# Cloud-Arcade
Cloud Arcade is a cloud gaming web application, designed to rekindle the
joy of classic retro games with unparalleled accessibility. This innovative
platform allows users to effortlessly dive into beloved titles ike Pacman,
Space Invaders etc without the need for any downloads or installations
Behind the scenes, each game is encapsulated within a Docker
container, ensuring portability and robust isolation. These containers are
thoughtfully deployed on Amazon EC2 instances, efficiently managed by
Elastic Beanstalk, providing auto-scaling capabilities to adapt to varying
user loads seamlessly.
The front-end website is hosted on Amazon S3 buckets, offering
lightning-fast and reliable static file serving to guarantee users minimal
load times and a responsive interface. When a user clicks on a game icon,
a new tab is launched, utilizing the EC2 endpoint to provide a seamless
transition into the world of retro gaming. This clever combination of
Docker containerization, AWS infrastructure, and dynamic frontend
hosting ensures that Cloud Arcade delivers a hassle-free and immersive
gaming experience to users.

Demo: https://youtu.be/1kXqqJ-L73M?si=IU-UlMiPmHXpnfph
