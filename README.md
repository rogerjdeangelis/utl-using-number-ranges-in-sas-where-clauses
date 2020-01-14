# utl-using-number-ranges-in-sas-where-clauses
Using number ranges in sas where clauses
    Using number ranges in sas where clauses                                                      
                                                                                                  
      I did not know you could do this                                                            
                                                                                                  
        where var in (1:20, 30:33, 50:65);                                                        
                                                                                                  
    github                                                                                        
    https://tinyurl.com/tjp9m6w                                                                   
    https://github.com/rogerjdeangelis/utl-using-number-ranges-in-sas-where-clauses               
                                                                                                  
    Draycut profile                                                                               
    https://communities.sas.com/t5/user/viewprofilepage/user-id/31304                             
                                                                                                  
    SAS Forum                                                                                     
    https://tinyurl.com/yx6p67na                                                                  
    https://communities.sas.com/t5/New-SAS-User/WHERE-IN-number-another-number/m-p/617174         
                                                                                                  
    *_                   _                                                                        
    (_)_ __  _ __  _   _| |_                                                                      
    | | '_ \| '_ \| | | | __|                                                                     
    | | | | | |_) | |_| | |_                                                                      
    |_|_| |_| .__/ \__,_|\__|                                                                     
            |_|                                                                                   
    ;                                                                                             
                                                                                                  
    data have;                                                                                    
       var=20; output;                                                                            
       var=21; output;                                                                            
    run;                                                                                          
                                                                                                  
    Up to 40 obs WORK.HAVE total obs=2                                                            
                                                                                                  
    Obs    VAR                                                                                    
                                                                                                  
     1      20                                                                                    
     2      21                                                                                    
                                                                                                  
    *            _               _                                                                
      ___  _   _| |_ _ __  _   _| |_                                                              
     / _ \| | | | __| '_ \| | | | __|                                                             
    | (_) | |_| | |_| |_) | |_| | |_                                                              
     \___/ \__,_|\__| .__/ \__,_|\__|                                                             
                    |_|                                                                           
    ;                                                                                             
                                                                                                  
    Up to 40 obs WORK.WANT total obs=1                                                            
                                                                                                  
                | RULE                                                                            
    Obs    VAR  |                                                                                 
                |                                                                                 
     1      20  | Subset for just var=20                                                          
                                                                                                  
    *          _       _   _                                                                      
     ___  ___ | |_   _| |_(_) ___  _ __                                                           
    / __|/ _ \| | | | | __| |/ _ \| '_ \                                                          
    \__ \ (_) | | |_| | |_| | (_) | | | |                                                         
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|                                                         
                                                                                                  
    ;                                                                                             
                                                                                                  
    data want;                                                                                    
        set have;                                                                                 
        where var in (1:20, 30:33, 50:65);                                                        
    run;                                                                                          
                                                                                                  
                                                                                                  
