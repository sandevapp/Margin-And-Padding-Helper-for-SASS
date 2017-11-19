Paste it to the scss file

     $spaceamounts: (5, 10, 15, 20, 25, 30, 35, 40, 45, 50, 75, 100); 
     $sides: (top, bottom, left, right);
  
     @each $space in $spaceamounts {    
       @each $side in $sides {
          .m-#{str-slice($side, 0, 1)}-#{$space} {
            margin-#{$side}: #{$space}px !important;
          }
  
          .p-#{str-slice($side, 0, 1)}-#{$space} {
            padding-#{$side}: #{$space}px !important;
          }
    
        }
      }

How to use 

    .m-t-15 gives MARGIN to the TOP 15 pixels
    .m-r-15 gives MARGIN to the RIGHT 15 pixels
    .m-l-15 gives MARGIN to the LEFT 15 pixels
    .m-b-15 gives MARGIN to the BOTTOM 15 pixels

    .p-t-15 gives PADDING to the TOP of 15 pixels
    .p-r-15 gives PADDING to the RIGHT of 15 pixels
    .p-l-15 gives PADDING to the LEFT of 15 pixels
    .p-b-15 gives PADDING to the BOTTOM of 15 pixels
