<section>
        <div class="container">
            <h2>FAQ</h2>
            <!-- accordion class -->
            <div class="question">
                <div class="question1" id="questionid1">
                    <a class="questionlink" href="#questionid1">
                        How to reset password?
                        <i class="icon ion-md-arrow-dropdown"></i>
                        
                    </a>
                    <div class="answer">
                        <p>
                        Please click on the 'Forgot Password' link below to initiate the password reset process. An email will be sent to your registered email address with instructions on how to reset your password. 
                        </p>
                    </div>
                </div>

                <div class="question1" id="questionid2">
                    <a class="questionlink" href="#questionid2">
                        How does the buying process happen?
                        <i class="icon ion-md-arrow-dropdown"></i>
                        
                    </a>
                    <div class="answer">
                        <p>
                        The buying and selling process is directly done between buyer and seller , to make our platfrom more user friendly. 
                        </p>
                    </div>
                </div>


                <div class="question1" id="questionid3">
                    <a class="questionlink" href="#questionid3">
                        How to create an account?
                        <i class="icon ion-md-arrow-dropdown"></i>
                        
                    </a>
                    <div class="answer">
                        <p>
                        To create an account , click "Sign up" section in top right corner of the page.
                        Then enter required details to create an account.
                        </p>
                    </div>
                </div>

                <div class="question1" id="questionid4">
                    <a class="questionlink" href="#questionid4">
                        Can I also sell my handicrafts?
                        <i class="icon ion-md-arrow-dropdown"></i>
                        
                    </a>
                    <div class="answer">
                        <p>
                        Not only fruits and veggies but any type of products that are locally made 
                        can be sold at our site !
                        </p>
                    </div>
                </div>
            </div>       
        </div>
    </section>   

<style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

h2{
    font-size: 50px;
    color: 314673;
    margin: 2% auto;
}

section{
    width: 100%;
    height: 100vh;
    background-color: rgb(255, 255, 255);
    display:flex;
    align-items: center;
    justify-content: center;


}

.container{
    width: 100%;
    max-width: 70rem;
    margin: 0 auto;
    padding : 0 1.5rem;
}

.question1{
   background-color: #314673; 
   margin-bottom: 1rem;
   border-radius: .4rem;
   padding: 1rem;
   box-shadow: .5rem 1rem .5rem rgba(0, 0, 0,.1)  ;
   
}

.questionlink{

    font-size: 1.6rem;
    color:rgb(255, 255, 255);
    background-color:#314673;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    text-decoration: none;
    padding: 1rem 0;

}

.questionlink i{
   padding-bottom: 0.5rem;

}

.answer{
    max-height: 0;
    overflow:hidden;
    position: relative;
    background-color:#212f4d;
    border-radius: 1rem;
}



.answer p{
    color: rgb(255, 255, 255);
    padding:1rem;
}

.question1:target .answer{
    max-height: 20rem;
}
</style>