# Mon framework

## Couleurs:

### Background:

    - .bg-white
    - .bg-black
    - .bg-red
    - .bg-blue
    - .bg-green
    - .bg-orange

## Éléments:

## Layouts:

### Headers:

    -Classic:
    
    --HTML:
    
    ```
    <header class="classic-header-layout bg-orange">
        <figure>
            <img src="https://picsum.photos/id/452/300/300" alt="Logo du site">
            <figcaption>Logo du site</figcaption>
        </figure>
        <nav class="white-links">
            <ul>
                <li><a href="">Home<span class="fa-solid fa-arrow-right"></span></a></li>
                <li><a href="">About Me<span class="fa-solid fa-arrow-right"></span></a></li>
                <li><a href="">Contact<span class="fa-solid fa-arrow-right"></span></a></li>
                <li><a href="">Blog<span class="fa-solid fa-arrow-right"></span></a></li>
            </ul>
        </nav>
        <nav class="white-links">
            <ul>
                <li><a href=""><span>Facebook</span><span class="fa-brands fa-facebook"></span></a></li>
                <li><a href=""><span>Linkedin</span><span class="fa-brands fa-linkedin"></span></a></li>
                <li><a href=""><span>Github</span><span class="fa-brands fa-github"></span></a></li>
            </ul>
        </nav>
    </header>
    ```
    
    --CSS:
    
    ```
    .classic-header-layout{
    
        display: grid;
        grid-template-columns: .1fr .7fr .2fr;
        grid-template-row: 1fr 1fr 1fr;
        width: 100%;
        max-height: 12vh;
        padding: 1vh 2vw;
        
        &>figure{
            
            grid-column: 1/2;
            grid-row: 1/4;
            max-height: 10vh;
            
            &>img{
                
                max-height: 100%;
                border-radius: 20px;
            }
            
            &>figcaption{
                
                display: none;
            }
        }
        
        &>nav:first-of-type{
            
            grid-column: 2/3;
            grid-row: 2/3;
            
            &>ul{
            
                display: flex;
                flex-direction: row;
                align-items: center;
                justify-content: space-evenly;
                
                &>li{
                    
                    &>a{
                        
                        text-decoration: none;
                        text-transform: uppercase;
                        font-weight: bold;
                        padding: 1.5vh 2vw;
                        border-radius: 5px;
                        transition: all 0.2s ease-out;
                        
                        &>span{
                            
                            display: none;
                        }
                        
                        &:hover{
                            
                            border-bottom: solid 3px;
                            border-left: solid 3px;
                            
                            &>span{
                                
                                margin-left: .5vw;
                                display: inline-block;
                            }
                        }
                    }
                }
            }
        }
        
        &>nav:last-of-type{
            
            grid-column: 3/4;
            grid-row: 2/3;
            
            &>ul{
            
                display: flex;
                flex-direction: row;
                align-items: center;
                justify-content: space-evenly;
                
                &>li{
                    
                    &>a{
                        
                        text-decoration: none;
                        text-transform: capitalize;
                        font-weight: bold;
                        display: flex;
                        flex-direction: row;
                        
                        &>span:first-of-type{
                            
                            display: none;
                        }
                        
                        &>span:last-of-type{
                            
                            margin-left: .3vw;
                        }
                        
                        &:hover{
                            
                            &>span:first-of-type{
                            
                                display: inline-block;
                            }
                        }
                    }
                }
            }
        }
    }
    ```