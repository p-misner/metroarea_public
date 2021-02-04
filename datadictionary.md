# useful variables in geojson files (city_name+'.geojson'):

  __a__	  
  `food/grocery/health+ ‘_acc_score’`	 | accessibility score for food/grocery/health in pre-covid situation.  
  new: `food/grocery/health+ ‘_acc_score’`

  __b__	  
  `food/grocery/health+ ‘2_acc_score’`	 | accessibility score under business closure.  
  new: `[food/grocery/health]+[bc] +‘_acc_score’`

  __c__	  
  `food/grocery/health+'2_Monday_score'`	| accessibility score under business closure+social distancing.  
  new: `[food/grocery/health]+[bcsd] +‘_acc_score’`	

  __d__   
  `food/grocery/health+'2_compete2_score'`  | accessibility score under business closure+social distancing + bus delays(headways*2).  
  new: `[food/grocery/health]+[bcsdpt1.5] +‘_acc_score’`  

  __e__    
  `food/grocery/health+'2_compete1.5_score'`  | accessibility score under business closure+social distancing + bus delays(headways*1.5).  
  new: `[food/grocery/health]+[bcsdpt1.5] +‘_acc_score’` 


  __f__	 
  `c_'+food/grocery/health+'influence'`	  | comparison of food/grocery/health accessibility rank change under {business closure}: (b-a)  


  __g__	 
  `sd_'+food/grocery/health+'influence'`	 | comparison of food/grocery/health accessibility rank change under {social distancing}: (c-b)	 
  new:`[food/grocery/health]+[sd] +‘_acc_score’`   


  h	 `all_'+food/grocery/health+'influence'`	| comparison of food/grocery/health accessibility rank change under {business closure + social distancing}: (c-a)	 

  i  `'bus_delay_'+food/grocery/health +'influence_2'` | comparison of food/grocery/health accessibility rank change under {bus delay (headways*2)}:(d-c)



# useful variables in acc2dis.csv:

  a `int_dis` | distance to a city center

  b `food/grocery/health+'2_acc_flag'` | the average accessibility at given 'int_dis' under business closure

  c f`ood/grocery/health+'2_Monday_flag'` | the average accessibility at given 'int_dis' under business closure + social distancing


# useful variables in city+'_accessibilty_races.csv':

  a `accessibility` |the accessibility value under business closure + social distancing

  b `race`  | the income and race attribute, black/white --race, poverty/non_poverty--income level

  c `num`  | the size of population in the given race 'race' with accessibility the 'accessibility' score



  using the data store in this file, we can show the accessibility distribution in different socioeconomics group. e.g.,for black_non_poverty,

  accessibility  num  race

  1             3    black_non_poverty

  2             4    black_non_poverty

  the average accessibility is (1*3+2*4)/(3+4)

  

# useful variables in gap.csv:

  This file describes the average accessibility difference in percentage for different races under different situations. The description for variables could be found in this file.