# IAAA

Model: "model"
__________________________________________________________________________________________________
 Layer (type)                Output Shape                 Param #   Connected to                  
==================================================================================================
 input_1 (InputLayer)        [(None, 64, 64, 3)]          0         []                            
                                                                                                  
 conv2d_8 (Conv2D)           (None, 64, 64, 8)            224       ['input_1[0][0]']             
                                                                                                  
 conv2d_10 (Conv2D)          (None, 64, 64, 8)            608       ['input_1[0][0]']             
                                                                                                  
 conv2d_13 (Conv2D)          (None, 64, 64, 8)            224       ['input_1[0][0]']             
                                                                                                  
 batch_normalization (Batch  (None, 64, 64, 8)            32        ['conv2d_8[0][0]']            
 Normalization)                                                                                   
                                                                                                  
 batch_normalization_2 (Bat  (None, 64, 64, 8)            32        ['conv2d_10[0][0]']           
 chNormalization)                                                                                 
                                                                                                  
 batch_normalization_5 (Bat  (None, 64, 64, 8)            32        ['conv2d_13[0][0]']           
 chNormalization)                                                                                 
                                                                                                  
 conv2d_9 (Conv2D)           (None, 64, 64, 8)            584       ['batch_normalization[0][0]'] 
                                                                                                  
 conv2d_11 (Conv2D)          (None, 64, 64, 8)            584       ['batch_normalization_2[0][0]'
                                                                    ]                             
                                                                                                  
 conv2d_12 (Conv2D)          (None, 64, 64, 8)            32        ['input_1[0][0]']             
                                                                                                  
 conv2d_14 (Conv2D)          (None, 64, 64, 8)            72        ['batch_normalization_5[0][0]'
                                                                    ]                             
                                                                                                  
 batch_normalization_1 (Bat  (None, 64, 64, 8)            32        ['conv2d_9[0][0]']            
 chNormalization)                                                                                 
                                                                                                  
 batch_normalization_3 (Bat  (None, 64, 64, 8)            32        ['conv2d_11[0][0]']           
 chNormalization)                                                                                 
                                                                                                  
 batch_normalization_4 (Bat  (None, 64, 64, 8)            32        ['conv2d_12[0][0]']           
 chNormalization)                                                                                 
                                                                                                  
 batch_normalization_6 (Bat  (None, 64, 64, 8)            32        ['conv2d_14[0][0]']           
 chNormalization)                                                                                 
                                                                                                  
 concatenate (Concatenate)   (None, 64, 64, 32)           0         ['batch_normalization_1[0][0]'
                                                                    , 'batch_normalization_3[0][0]
                                                                    ',                            
                                                                     'batch_normalization_4[0][0]'
                                                                    , 'batch_normalization_6[0][0]
                                                                    ']                            
                                                                                                  
 conv2d (Conv2D)             (None, 64, 64, 8)            224       ['input_1[0][0]']             
                                                                                                  
 conv2d_15 (Conv2D)          (None, 64, 64, 16)           4624      ['concatenate[0][0]']         
                                                                                                  
 conv2d_17 (Conv2D)          (None, 64, 64, 16)           12816     ['concatenate[0][0]']         
                                                                                                  
 conv2d_20 (Conv2D)          (None, 64, 64, 16)           4624      ['concatenate[0][0]']         
                                                                                                  
 conv2d_1 (Conv2D)           (None, 64, 64, 8)            584       ['conv2d[0][0]']              
                                                                                                  
 batch_normalization_7 (Bat  (None, 64, 64, 16)           64        ['conv2d_15[0][0]']           
 chNormalization)                                                                                 
                                                                                                  
 batch_normalization_9 (Bat  (None, 64, 64, 16)           64        ['conv2d_17[0][0]']           
 chNormalization)                                                                                 
                                                                                                  
 batch_normalization_12 (Ba  (None, 64, 64, 16)           64        ['conv2d_20[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 max_pooling2d (MaxPooling2  (None, 32, 32, 8)            0         ['conv2d_1[0][0]']            
 D)                                                                                               
                                                                                                  
 conv2d_16 (Conv2D)          (None, 64, 64, 16)           2320      ['batch_normalization_7[0][0]'
                                                                    ]                             
                                                                                                  
 conv2d_18 (Conv2D)          (None, 64, 64, 16)           2320      ['batch_normalization_9[0][0]'
                                                                    ]                             
                                                                                                  
 conv2d_19 (Conv2D)          (None, 64, 64, 16)           528       ['concatenate[0][0]']         
                                                                                                  
 conv2d_21 (Conv2D)          (None, 64, 64, 16)           272       ['batch_normalization_12[0][0]
                                                                    ']                            
                                                                                                  
 conv2d_2 (Conv2D)           (None, 32, 32, 16)           1168      ['max_pooling2d[0][0]']       
                                                                                                  
 batch_normalization_8 (Bat  (None, 64, 64, 16)           64        ['conv2d_16[0][0]']           
 chNormalization)                                                                                 
                                                                                                  
 batch_normalization_10 (Ba  (None, 64, 64, 16)           64        ['conv2d_18[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 batch_normalization_11 (Ba  (None, 64, 64, 16)           64        ['conv2d_19[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 batch_normalization_13 (Ba  (None, 64, 64, 16)           64        ['conv2d_21[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 conv2d_3 (Conv2D)           (None, 32, 32, 16)           2320      ['conv2d_2[0][0]']            
                                                                                                  
 max_pooling2d_3 (MaxPoolin  (None, 32, 32, 16)           0         ['batch_normalization_8[0][0]'
 g2D)                                                               ]                             
                                                                                                  
 max_pooling2d_4 (MaxPoolin  (None, 32, 32, 16)           0         ['batch_normalization_10[0][0]
 g2D)                                                               ']                            
                                                                                                  
 max_pooling2d_5 (MaxPoolin  (None, 32, 32, 16)           0         ['batch_normalization_11[0][0]
 g2D)                                                               ']                            
                                                                                                  
 max_pooling2d_6 (MaxPoolin  (None, 32, 32, 16)           0         ['batch_normalization_13[0][0]
 g2D)                                                               ']                            
                                                                                                  
 max_pooling2d_1 (MaxPoolin  (None, 16, 16, 16)           0         ['conv2d_3[0][0]']            
 g2D)                                                                                             
                                                                                                  
 concatenate_1 (Concatenate  (None, 32, 32, 64)           0         ['max_pooling2d_3[0][0]',     
 )                                                                   'max_pooling2d_4[0][0]',     
                                                                     'max_pooling2d_5[0][0]',     
                                                                     'max_pooling2d_6[0][0]']     
                                                                                                  
 conv2d_4 (Conv2D)           (None, 16, 16, 32)           4640      ['max_pooling2d_1[0][0]']     
                                                                                                  
 conv2d_22 (Conv2D)          (None, 32, 32, 32)           18464     ['concatenate_1[0][0]']       
                                                                                                  
 conv2d_24 (Conv2D)          (None, 32, 32, 32)           51232     ['concatenate_1[0][0]']       
                                                                                                  
 conv2d_27 (Conv2D)          (None, 32, 32, 32)           18464     ['concatenate_1[0][0]']       
                                                                                                  
 conv2d_5 (Conv2D)           (None, 16, 16, 32)           9248      ['conv2d_4[0][0]']            
                                                                                                  
 batch_normalization_14 (Ba  (None, 32, 32, 32)           128       ['conv2d_22[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 batch_normalization_16 (Ba  (None, 32, 32, 32)           128       ['conv2d_24[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 batch_normalization_19 (Ba  (None, 32, 32, 32)           128       ['conv2d_27[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 max_pooling2d_2 (MaxPoolin  (None, 8, 8, 32)             0         ['conv2d_5[0][0]']            
 g2D)                                                                                             
                                                                                                  
 conv2d_23 (Conv2D)          (None, 32, 32, 32)           9248      ['batch_normalization_14[0][0]
                                                                    ']                            
                                                                                                  
 conv2d_25 (Conv2D)          (None, 32, 32, 32)           9248      ['batch_normalization_16[0][0]
                                                                    ']                            
                                                                                                  
 conv2d_26 (Conv2D)          (None, 32, 32, 32)           2080      ['concatenate_1[0][0]']       
                                                                                                  
 conv2d_28 (Conv2D)          (None, 32, 32, 32)           1056      ['batch_normalization_19[0][0]
                                                                    ']                            
                                                                                                  
 conv2d_6 (Conv2D)           (None, 8, 8, 64)             18496     ['max_pooling2d_2[0][0]']     
                                                                                                  
 batch_normalization_15 (Ba  (None, 32, 32, 32)           128       ['conv2d_23[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 batch_normalization_17 (Ba  (None, 32, 32, 32)           128       ['conv2d_25[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 batch_normalization_18 (Ba  (None, 32, 32, 32)           128       ['conv2d_26[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 batch_normalization_20 (Ba  (None, 32, 32, 32)           128       ['conv2d_28[0][0]']           
 tchNormalization)                                                                                
                                                                                                  
 conv2d_7 (Conv2D)           (None, 8, 8, 64)             36928     ['conv2d_6[0][0]']            
                                                                                                  
 max_pooling2d_7 (MaxPoolin  (None, 16, 16, 32)           0         ['batch_normalization_15[0][0]
 g2D)                                                               ']                            
                                                                                                  
 max_pooling2d_8 (MaxPoolin  (None, 16, 16, 32)           0         ['batch_normalization_17[0][0]
 g2D)                                                               ']                            
                                                                                                  
 max_pooling2d_9 (MaxPoolin  (None, 16, 16, 32)           0         ['batch_normalization_18[0][0]
 g2D)                                                               ']                            
                                                                                                  
 max_pooling2d_10 (MaxPooli  (None, 16, 16, 32)           0         ['batch_normalization_20[0][0]
 ng2D)                                                              ']                            
                                                                                                  
 conv2d_transpose (Conv2DTr  (None, 16, 16, 64)           16448     ['conv2d_7[0][0]']            
 anspose)                                                                                         
                                                                                                  
 concatenate_2 (Concatenate  (None, 16, 16, 128)          0         ['max_pooling2d_7[0][0]',     
 )                                                                   'max_pooling2d_8[0][0]',     
                                                                     'max_pooling2d_9[0][0]',     
                                                                     'max_pooling2d_10[0][0]']    
                                                                                                  
 concatenate_3 (Concatenate  (None, 16, 16, 224)          0         ['conv2d_transpose[0][0]',    
 )                                                                   'conv2d_5[0][0]',            
                                                                     'concatenate_2[0][0]']       
                                                                                                  
 conv2d_29 (Conv2D)          (None, 16, 16, 64)           129088    ['concatenate_3[0][0]']       
                                                                                                  
 conv2d_30 (Conv2D)          (None, 16, 16, 64)           36928     ['conv2d_29[0][0]']           
                                                                                                  
 conv2d_transpose_1 (Conv2D  (None, 32, 32, 32)           8224      ['conv2d_30[0][0]']           
 Transpose)                                                                                       
                                                                                                  
 concatenate_4 (Concatenate  (None, 32, 32, 112)          0         ['conv2d_transpose_1[0][0]',  
 )                                                                   'conv2d_3[0][0]',            
                                                                     'concatenate_1[0][0]']       
                                                                                                  
 conv2d_31 (Conv2D)          (None, 32, 32, 32)           32288     ['concatenate_4[0][0]']       
                                                                                                  
 conv2d_32 (Conv2D)          (None, 32, 32, 32)           9248      ['conv2d_31[0][0]']           
                                                                                                  
 conv2d_transpose_2 (Conv2D  (None, 64, 64, 16)           2064      ['conv2d_32[0][0]']           
 Transpose)                                                                                       
                                                                                                  
 concatenate_5 (Concatenate  (None, 64, 64, 56)           0         ['conv2d_transpose_2[0][0]',  
 )                                                                   'conv2d_1[0][0]',            
                                                                     'concatenate[0][0]']         
                                                                                                  
 conv2d_33 (Conv2D)          (None, 64, 64, 16)           8080      ['concatenate_5[0][0]']       
                                                                                                  
 conv2d_34 (Conv2D)          (None, 64, 64, 16)           2320      ['conv2d_33[0][0]']           
                                                                                                  
 conv2d_35 (Conv2D)          (None, 64, 64, 3)            51        ['conv2d_34[0][0]']           
                                                                                                  
==================================================================================================
Total params: 459539 (1.75 MB)
Trainable params: 458755 (1.75 MB)
Non-trainable params: 784 (3.06 KB)