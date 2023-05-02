Download Link: https://assignmentchef.com/product/solved-comp9044-lab-3
<br>



Before the lab you should re-read the relevant lecture slides and their accompanying examples.

Create a new directory for this lab called lab03, change to this directory, and fetch the provided code for this week by running these commands:

$ <strong>mkdir lab03</strong>

$ <strong>cd lab03</strong>

$ <strong>2041 fetch lab03</strong>

Or, if you’re not working on CSE, you can download the provided code as a <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/lab/03/provided.zip">zip</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/lab/03/provided.zip">file</a> or a <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/lab/03/provided.tar">tar</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/lab/03/provided.tar">file</a>.

Write a shell script jpg2png.sh which converts all images in <a href="https://en.wikipedia.org/wiki/JPEG">JPEG</a> format in the current directory to <a href="https://en.wikipedia.org/wiki/Portable_Network_Graphics">PNG</a> format.

You can assume that JPEG files and only JPEG files have the suffix jpg.

If the conversion is succesful the JPEG file should be removed.

Your script should stop with the error message shown below and exit status 1 if the PNG file already exists.

<table width="961">

 <tbody>

  <tr>

   <td width="961">$ <strong>wget https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/jpg2png/images.zip</strong>$ <strong>unzip images.zip</strong> Archive:  images.zip   inflating: Johannes Vermeer – The Girl With The Pearl Earring.jpg   inflating: nautilus.jpg   inflating: panic.jpg   inflating: penguins.jpg   inflating: shell.jpg   inflating: stingray.jpg   inflating: treefrog.jpg$ <strong>./jpg2png.sh</strong>$ <strong>ls</strong>‘Johannes Vermeer – The Girl With The Pearl Earring.png’   jpg2png.sh     panic.png  shell.png      treefrog.png  images.zip                        nautilus.png   penguins.png   stingray.png $ <strong>wget https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/jpg2png//penguins.jpg</strong>$ <strong>ls</strong>‘Johannes Vermeer – The Girl With The Pearl Earring.png’   jpg2png.sh     panic.png  penguins.png   stingray.png  images.zip                        nautilus.png   penguins.jpg   shell.png      treefrog.png$ <strong>./jpg2png.sh</strong> penguins.png already exists</td>

  </tr>

 </tbody>

</table>

When you think your program is working, you can use autotest to run some simple automated tests:

$ <strong>2041 autotest jpg2png</strong>

<h1>Autotest Results</h1>

95% of 447 students who have autotested jpg2png.sh so far, passed all autotest tests.

97% passed test <em>jpg2png_0</em>

96% passed test <em>jpg2png_1</em>

97% passed test <em>jpg2png_2</em>

96% passed test <em>jpg2png_3</em>

When you are finished working on this exercise, you must submit your work by running give:

$ <strong>give cs2041 lab03_jpg2png jpg2png.sh</strong>

before Tuesday 23 June 17 59 to obtain the marks for this lab exercise.

Write a shell script email_image.sh which given a list of image files as arguments displays them one-by-one. After the user has viewed each image the script should prompt the user for an e-mail address. If the user does enter an email address, the script should prompt the user for a message to accompany the image and then send the image to the specified e-mail address.

$ <strong>./email_image.sh penguins.png treefrog.png</strong>

Address to e-mail this image to? <strong><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="4d2c23293f283a390d2e3e286338233e3a63282938632c38">[email protected]</a></strong> Message to accompany image? <strong>Penguins are cool.</strong> penguins.png sent to <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2d4c43495f485a596d4e5e480358435e5a03484958034c58">[email protected]</a>

Address to e-mail this image to? <strong><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="5b3a353f293e2c2f1b38283e752e35282c753e3f2e753a2e">[email protected]</a></strong> Message to accompany image? <strong>This is a White-lipped Tree Frog</strong> treefrog.png sent to <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="1f7e717b6d7a686b5f7c6c7a316a716c68317a7b6a317e6a">[email protected]</a>

<h1>Hints</h1>

The program <a href="https://manpages.debian.org/jump?q=display.1"><em>displa</em></a><a href="https://manpages.debian.org/jump?q=display.1"><em>y</em></a><a href="https://manpages.debian.org/jump?q=display.1"><em>(1)</em></a> can be used to view image files

The program <a href="https://manpages.debian.org/jump?q=mutt.1"><em>mutt</em></a><a href="https://manpages.debian.org/jump?q=mutt.1"><em>(1)</em></a> can be used to send mail from the command line including attachments, for example:

$ <strong>echo ‘Penguins are cool.’|mutt -s ‘penguins!’ -e ‘set copy=no’ -a penguins.png — <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="b9d7d6dbd6ddc0f9d7d6ced1dccbdc97dad6d4">[email protected]</a></strong>

There is no autotest and no automarking of this question.

<a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">When</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">you</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">are</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">finished</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">working</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">on</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">this</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">exercise</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">,</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">demonstrate</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">your</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">work</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">to</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">another</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">student</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">in</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">your</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">lab</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">and</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">ask</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">them</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">to</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">enter</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">a</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">peer assessment</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">.</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/"> It</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">is</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">preferred</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">you</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">d</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">o </a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">this</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">during</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">your</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">lab</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">,</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">but</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">if</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">this</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">is</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">not</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">possible</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">you</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">may</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">demonstrate</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">your</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">work</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">to</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">any</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_email_image/">other </a>COMP(2041|9044) student before Tuesday 23 June 17 59. Note, you must also submit the work with give.

When you are finished working on this exercise, you must submit your work by running give:

$ <strong>give cs2041 lab03_email_image email_image.sh</strong>

before Tuesday 23 June 17 59 to obtain the marks for this lab exercise.

Write a shell script date_image.sh which, given a list of image files as arguments, changes each file so it has a label added to the image indicating the time it was taken. You can assume the last-modification time of the image file is the time it was taken.

So for example if we run these commands:

$ <strong>cp -p /web/cs2041/20T2/activities/date_image/penguins.jpg  .</strong>

$ <strong>ls -l penguins.jpg </strong>

-rw-r–r– 1 andrewt andrewt 58092 Mar 16 16:08 penguins.jpg

$ <strong>./date_image.sh penguins.jpg</strong>

$ <strong>display  penguins.jpg </strong>

There is no autotest and no automarking of this question.

<a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">When</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">you</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">are</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">finished</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">working</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">on</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">this</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">exercise</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">,</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">demonstrate</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">your</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">work</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">to</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">another</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">student</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">in</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">your</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">lab</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">and</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">ask</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">them</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">to</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">enter</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">a</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">peer assessment</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">.</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/"> It</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">is</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">preferred</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">you</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">d</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">o </a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">this</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">during</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">your</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">lab</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">,</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">but</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">if</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">this</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">is</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">not</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">possible</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">you</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">may</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">demonstrate</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">your</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">work</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">to</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">any</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/peer_assess/lab03_date_image/">other </a>COMP(2041|9044) student before Tuesday 23 June 17 59. Note, you must also submit the work with give.

When you are finished working on this exercise, you must submit your work by running give:

$ <strong>give cs2041 lab03_date_image date_image.sh</strong>

before Tuesday 23 June 17 59 to obtain the marks for this lab exercise.

Andrew regularly spends time far from the internet and streaming music services such as Spotify, so he has a <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">lar</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">g</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">e</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">c</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">o</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">llection</a> of <a href="https://en.wikipedia.org/wiki/MP3">MP</a><a href="https://en.wikipedia.org/wiki/MP3">3 </a>files containing music.

Andrew has a problem: the <a href="https://en.wikipedia.org/wiki/ID3">ID</a><a href="https://en.wikipedia.org/wiki/ID3">3</a> tags in the <a href="https://en.wikipedia.org/wiki/MP3">MP</a><a href="https://en.wikipedia.org/wiki/MP3">3</a> files in his music collection are incorrect. Unfortunately Andrew’s favourite player software organises music using the information from these <a href="https://en.wikipedia.org/wiki/ID3">ID</a><a href="https://en.wikipedia.org/wiki/ID3">3</a> tags. Your task it to fix Andrew’s problem by set the <a href="https://en.wikipedia.org/wiki/ID3">ID</a><a href="https://en.wikipedia.org/wiki/ID3">3</a> tags to the correct values. Fortunately the correct value for the tags can be retrieved from the file names and the names of the directories the files are in.

Your task is to write a shell script tag_music.sh, which sets the ID3 tags of MP3 files using the information from file names and directory names.

You’ll first need to make a copy of Andrew’s music collection.

Download <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">music</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">.</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">zip</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/music.zip">,</a> or copy it to your CSE account using the following command:

$ <strong>cp -n /web/cs2041/20T2/activities/tag_music/music.zip .</strong>

You assume the names of files and directories follow a standard format. You can determine this format by look at ethe files in Andrew’s music collection.

$ <strong>unzip music.zip</strong> Archive:  music.zip    creating: music/    creating: music/Triple J Hottest 100, 2007/   inflating: music/Triple J Hottest 100, 2007/2 – Straight Lines – Silverchair.mp3   inflating: music/Triple J Hottest 100, 2007/10 – Don’t Fight It – The Panics.mp3  <em>…</em>

The command id3 can be used to list the value of ID3 tags in an MP3 file. For example:

$ <strong>id3 -l ‘music/Triple J Hottest 100, 2013/1 – Riptide – Vance Joy.mp3’</strong> music/Triple J Hottest 100, 2013/1 – Riptide – Vance Joy.mp3:

Title  : Andrew Rocks                    Artist: Andrew

Album  : Best of Andrew                  Year: 2038, Genre: Unknown (255) Comment:                                 Track: 42

But, as you can see, the ID3 tags of this music file have been accidentally over-written. The ID3 tags <em>should</em> be:

$ <strong>id3 -l ‘music/Triple J Hottest 100, 2013/1 – Riptide – Vance Joy.mp3’</strong> music/Triple J Hottest 100, 2013/1 – Riptide – Vance Joy.mp3:

Title  : Riptide                         Artist: Vance Joy

Album  : Triple J Hottest 100, 2013      Year: 2013, Genre: Unknown (255) Comment:                                 Track: 1

Fortunately, all the information needed to fix the ID3 tags is available in the name of the file and the name of the directory it is in.

You will write a shell script tag_music.sh which takes the name of 1 or more directories as arguments and fixes the ID3 tags of the all MP3 files in that directory. For example:

<table width="961">

 <tbody>

  <tr>

   <td width="961">$ <strong>./tag_music.sh ‘music/Triple J Hottest 100, 2015’</strong>$ <strong>id3 -l ‘music/Triple J Hottest 100, 2015/4 – The Less I Know the Better – Tame Impala.mp3’</strong> music/Triple J Hottest 100, 2015/4 – The Less I Know the Better – Tame Impala.mp3:Title  : The Less I Know the Better      Artist: Tame ImpalaAlbum  : Triple J Hottest 100, 2015      Year: 2015, Genre: Unknown (255)Comment:                                 Track: 4$ <strong>./tag_music.sh music/*</strong>$ <strong>id3 -l ‘music/Triple J Hottest 100, 1995/10 – Greg! The Stop Sign!! – TISM.mp3’</strong> music/Triple J Hottest 100, 1995/10 – Greg! The Stop Sign!! – TISM.mp3:Title  : Greg! The Stop Sign!!           Artist: TISMAlbum  : Triple J Hottest 100, 1995      Year: 1995, Genre: Unknown (255)Comment:                                 Track: 10$ <strong>id3 -l ‘music/Triple J Hottest 100, 1999/1 – These Days – Powderfinger.mp3’</strong> music/Triple J Hottest 100, 1999/1 – These Days – Powderfinger.mp3:Title  : These Days                      Artist: Powderfinger Album  : Triple J Hottest 100, 1999      Year: 1999, Genre: Unknown (255)Comment:                                 Track: 1$ <strong>id3 -l ‘music/Triple J Hottest 100, 2012/2 – Little Talks – Of Monsters and Men.mp3’</strong> music/Triple J Hottest 100, 2012/2 – Little Talks – Of Monsters and Men.mp3: Title  : Little Talks                    Artist: Of Monsters and Men Album  : Triple J Hottest 100, 2012      Year: 2012, Genre: Unknown (255)Comment:                                 Track: 2</td>

  </tr>

 </tbody>

</table>

Your script should determine <em>Title</em>, <em>Artist</em>, <em>Track</em>, <em>Album</em>, and <em>Year</em> from the directory and filename.

Your script should not change the <em>Genre</em> or <em>Comment</em> fields.

<h1>Hints</h1>

$ <strong>man id3 </strong><em>…</em>

cut almost works for extracting <em>Title</em> and <em>Album</em> from the filename.

Handling the few MP3 files correctly where using <sub>cut</sub> doesn’t work will be considered a challenge exercise.

It can be difficult debugging your script on Andrew’s music collection. In cases like these it usually worth creating a smaller data set for initial debugging. Such a tiny data set is available in <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">tin</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">y</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">_</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">music</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">.</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">zip</a> if you want to use it for debugging. This dataset is used in the first autotests.




2020/7/24first autotests.

Download <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">tin</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">y</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">_</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">music</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">.</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">zip</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/tag_music/tiny_music.zip">,</a> or copy it to your CSE account using the following command:

$ <strong>cp -n /web/cs2041/20T2/activities/tag_music/tiny_music.zip .</strong>

<table width="961">

 <tbody>

  <tr>

   <td width="961">$ <strong>unzip tiny_music.zip</strong> Archive:  tiny_music.zip    creating: tiny_music/    creating: tiny_music/Album1, 2015/   inflating: tiny_music/Album1, 2015/2 – Little Talks – Of Monsters and Men.mp3   inflating: tiny_music/Album1, 2015/1 – Riptide – Vance Joy.mp3    creating: tiny_music/Album2, 2016/   inflating: tiny_music/Album2, 2016/2 – Royals – Lorde.mp3   inflating: tiny_music/Album2, 2016/1 – Hoops – The Rubens.mp3$ <strong>id3 -l tiny_music/*/*.mp3</strong> tiny_music/Album1, 2015/1 – Riptide – Vance Joy.mp3: Title  : Andrew Rocks                    Artist: AndrewAlbum  : Best of Andrew                  Year: 2038, Genre: Unknown (255) Comment:                                 Track: 42 tiny_music/Album1, 2015/2 – Little Talks – Of Monsters and Men.mp3:Title  : Andrew Rocks                    Artist: AndrewAlbum  : Best of Andrew                  Year: 2038, Genre: Unknown (255) Comment:                                 Track: 42 tiny_music/Album2, 2016/1 – Hoops – The Rubens.mp3: Title  : Andrew Rocks                    Artist: AndrewAlbum  : Best of Andrew                  Year: 2038, Genre: Unknown (255) Comment:                                 Track: 42 tiny_music/Album2, 2016/2 – Royals – Lorde.mp3:Title  : Andrew Rocks                    Artist: AndrewAlbum  : Best of Andrew                  Year: 2038, Genre: Unknown (255)Comment:                                 Track: 42$ <strong>./tag_music.sh tiny_music/* </strong>$ <strong>id3 -l tiny_music/*/*.mp3</strong> tiny_music/Album1, 2015/1 – Riptide – Vance Joy.mp3: Title  : Riptide                         Artist: Vance JoyAlbum  : Album1, 2015                    Year: 2015, Genre: Unknown (255) Comment:                                 Track: 1 tiny_music/Album1, 2015/2 – Little Talks – Of Monsters and Men.mp3:Title  : Little Talks                    Artist: Of Monsters and Men Album  : Album1, 2015                    Year: 2015, Genre: Unknown (255) Comment:                                 Track: 2 tiny_music/Album2, 2016/1 – Hoops – The Rubens.mp3:Title  : Hoops                           Artist: The Rubens Album  : Album2, 2016                    Year: 2016, Genre: Unknown (255) Comment:                                 Track: 1 tiny_music/Album2, 2016/2 – Royals – Lorde.mp3: Title  : Royals                          Artist: Lorde Album  : Album2, 2016                    Year: 2016, Genre: Unknown (255)Comment:                                 Track: 2</td>

  </tr>

 </tbody>

</table>

When you think your program is working, you can use autotest to run some simple automated tests:

$ <strong>2041 autotest tag_music</strong>

<h1>Autotest Results</h1>

72% of 106 students who have autotested tag_music.sh so far, passed all autotest tests.

79% passed test <em>1993_7</em>

88% passed test <em>1994</em>

80% passed test <em>1995_1996</em>

88% passed test <em>1999</em>

85% passed test <em>2009_2</em>

74% passed test <em>all</em>

88% passed test <em>tiny_album1</em> <em>tiny_album2</em>

84% passed test <em>tiny_both</em>

When you are finished working on this exercise, you must submit your work by running give:

$ <strong>give cs2041 lab03_tag_music tag_music.sh</strong>

before Tuesday 23 June 17 59 to obtain the marks for this lab exercise.

2020/7/24

The test data for the previous question is not really Andrew’s music collection. All the mp3 files contain identical contents. The directories and filenames were created from the source of this <a href="https://en.wikipedia.org/wiki/Triple_J_Hottest_100">web</a> <a href="https://en.wikipedia.org/wiki/Triple_J_Hottest_100">pa</a><a href="https://en.wikipedia.org/wiki/Triple_J_Hottest_100">g</a><a href="https://en.wikipedia.org/wiki/Triple_J_Hottest_100">e</a>.

Write a shell script create_music.sh which uses the above webpage to create exactly the same directories and files as in the test data set supplied above.

Your script should take 2 arguments: the name of an MP3 file to use as the contents of the MP3 files you create and the directory in which to create the test data. For example:

<table width="961">

 <tbody>

  <tr>

   <td width="961">$ <strong>wget https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/create_music/sample.mp3</strong>$ <strong>mkdir my_fake_music</strong>$ <strong>ls my_fake_music</strong>$ <strong>./create_music.sh sample.mp3 my_fake_music</strong>$ <strong>ls my_fake_music</strong>‘Triple J Hottest 100, 1993’  ‘Triple J Hottest 100, 1998’  ‘Triple J Hottest 100, 2003’  ‘Triple J Hottest 100, 2008’  ‘Triple J Hottest 100, 2013’‘Triple J Hottest 100, 1994’  ‘Triple J Hottest 100, 1999’  ‘Triple J Hottest 100, 2004’  ‘Triple J Hottest 100, 2009’  ‘Triple J Hottest 100, 2014’‘Triple J Hottest 100, 1995’  ‘Triple J Hottest 100, 2000’  ‘Triple J Hottest 100, 2005’  ‘Triple J Hottest 100, 2010’  ‘Triple J Hottest 100, 2015’‘Triple J Hottest 100, 1996’  ‘Triple J Hottest 100, 2001’  ‘Triple J Hottest 100, 2006’  ‘Triple J Hottest 100, 2011’  ‘Triple J Hottest 100, 2016’‘Triple J Hottest 100, 1997’  ‘Triple J Hottest 100, 2002’  ‘Triple J Hottest 100, 2007’  ‘Triple J Hottest 100,2012’  ‘Triple J Hottest 100, 2017’$ <strong>ls ‘my_fake_music/Triple J Hottest 100, 2017’</strong>‘1 – Humble – Kendrick Lamar.mp3’                ‘5 – The Deepest Sighs, the Frankest Shadows – Gang of Youths.mp3′’10 – What Can I Do If the Fire Goes Out? – Gang of Youths.mp3’  ‘6 – Green Light – Lorde.mp3’‘2 – Let Me Down Easy – Gang of Youths.mp3’          ‘7 – Go Bang – Pnau.mp3’‘3 – Chateau – Angus &amp; Julia Stone.mp3’              ‘8 – Sally – Thundamentals featuring Mataya.mp3’‘4 – Ubu – Methyl Ethel.mp3’                     ‘9 – Lay It on Me – Vance Joy.mp3’$ <strong>wget https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/create_music/music.zip</strong>$ <strong>unzip music.zip</strong> …$ <strong>diff -r music my_fake_music</strong>$</td>

  </tr>

 </tbody>

</table>

When you think your program is working, you can use autotest to run some simple automated tests:

$ <strong>2041 autotest create_music</strong>

<h1>Autotest Results</h1>

62% of 32 students who have autotested create_music.sh so far, passed the autotest test.

When you are finished working on this exercise, you must submit your work by running give:

$ <strong>give cs2041 lab03_create_music create_music.sh</strong>

before Tuesday 23 June 17 59 to obtain the marks for this lab exercise.

When you are finished each exercises make sure you submit your work by running give.

You can run give multiple times. Only your last submission will be marked.

Don’t submit any exercises you haven’t attempted.

2020/7/24

If you are working at home, you may find it more convenient to upload your work via <a href="https://cgi.cse.unsw.edu.au/~give/Student/give.php">g</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/give.php">ive</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/give.php">‘</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/give.php">s</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/give.php">web</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/give.php">interface</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/give.php">.</a>

Remember you have until Tuesday 23 June 17 59 59 to submit your work.

You cannot obtain marks by e-mailing your code to tutors or lecturers.

You check the files you have submitted <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/student/">here</a>.

Automarking will be run by the lecturer several days after the submission deadline, using test cases different to those autotest runs for you. (Hint: do your own testing as well as running autotest.)

<a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">After</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">automarking</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">is</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">run</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">by</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">the</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">lecturer</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">you</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">can</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">view</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">y</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">our</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">results</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">here</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">.</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">The</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">resulting</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">mark</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">will</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">also</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">be</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">available</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">via</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">g</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">ive</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">‘</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">s</a> <a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">web interface</a><a href="https://cgi.cse.unsw.edu.au/~give/Student/sturec.php">.</a>


