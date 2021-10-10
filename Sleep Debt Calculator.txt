const getSleepHours = (day) => {

day = day.toLowerCase();

switch(day){
case 'monday':    return 8 ;
case 'tuesday':   return 8 ;
case 'wednesday': return 8;
case 'thursday':  return 8 ;
case 'friday':    return 8 ;
case 'saturday':  return 8 ;
case 'sunday':    return 8 ;

default : return 'Enter a valid day';
}
  
}

const getActualSleepHours = () => {
let total = 0;

total += getSleepHours('monday');
total += getSleepHours('tuesday');
total += getSleepHours('wednesday');
total += getSleepHours('thursday');
total += getSleepHours('friday');
total += getSleepHours('saturday');
total += getSleepHours('sunday');

return total;
}

getIdealSleepHours = () => {

idealHours = 8;
return idealHours * 7;

}

const calculateSleepDebt = function (){
let actualSleepHours = getActualSleepHours();
let idealSleepHours = getIdealSleepHours();

if(actualSleepHours === idealSleepHours){
console.log('You got the perfect amount of sleep.');

}else if(actualSleepHours > idealSleepHours){
console.log('You got more sleep than needed. \n' + (actualSleepHours-idealSleepHours) + ' hours more to be precise.');

}else{
console.log('You need to get some rest.\n'+ (idealSleepHours - actualSleepHours) + ' hours of sleep will be ideal')

}

}

calculateSleepDebt();


