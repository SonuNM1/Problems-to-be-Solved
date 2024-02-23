  function removeSolutionNumber(text){
            const regex = /^(Sol\.\s*)\d+\.\s*/gm ; 
            text = text.replaceAll(regex, "$1") ; 
            return text ; 
        }

        function quesNoToQues(text){
            const regex = /^\d+\./ ;
            var lines = text.split('\n') ; 
            lines = lines.map((line)=>{
                if(regex.test(line)){
                    var temp = line.replace(regex, "Ques.") ; 
                    return (temp) ; 
                } else {
                    return (line) ; 
                }
            }) ; 

            return lines.join('\n') ; 
        }