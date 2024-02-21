let text = `
**Ques.** If  $ 0 < x < 5 $  and  $ 1 < y < 2 $ , then which of the following is true?

(a)  $ x+y <0 $ 
(b)  $ -3<2 x-3 y <4 $ 
(c)  $ -6<2 x-3 y <7 $ 
(d)  $ -3<3 x-y <2 $ 


</font>

</div>

- - -

<font size = "4">

Footer

</font>

</textarea>
</section>


<section data-markdown data-separator='======'>
<textarea data-template>

### <success>INEQUALITIES</success>

<div style="text-align:left">

- - -

<font size = "5.9">

**Sol.** (c)  $ 0 < x < 5 $ 

$ 0 < 2 x < 10 $ 

$ 1 < y < 2 $ 

...(2) (multiply (1) by 2)

-6 < -3 y < -3  

..(4) (multiply (3) by -3 )

Subtracting (4) from (2)

0-6 < 2 x-3 y < 10-3   i.e.,   -6 < 2 x-3 y < 7  .


</font>

</div>

- - -

<font size = "4">

Footer

</font>

</textarea>
</section>

<section data-markdown data-separator='======'>
<textarea data-template>

### <success>INEQUALITIES</success>

#### <Primary >Level - I</Primary >

<div style="text-align:left">

- - -

<font size = "5.9">

**Ques.** Which of the following is the solution set of  $ |2 x-3|<7 $  ?

(a)  $ \{x:-5 < x < 2\} $ 
(b)  $ \{x:-5 < x < 5\} $ 
(c)  $ \{x:-2 < x < 5\} $ 
(d)  {$x: x<-5 $  or  $ x >2 $} 
` ; 

const regex = /^\([a-d]\)/ ;
const regexOptionA = /^\(a\)/ ; 

let lines = text.split('\n') ; 

for(let i=0 ; i<lines.length ; i++){
    let line = lines[i] ; 
    
    if(line.match(regex)){
        if(line.match(regexOptionA)){
            lines[i] = `<p class="fragment">\n` + lines[i] + '$\\newline$' ; 
        }else{
        lines[i] += '$\\newline$' ;
        }
    }
}

let result = lines.join('\n') ; 

result += '</p>' ; 

console.log(result) ; 