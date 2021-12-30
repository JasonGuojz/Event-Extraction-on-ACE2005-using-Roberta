# Event Extraction on ACE2005 using Roberta

1. One CRF layer for trigger detection; 2. Concatenate trigerEmbd, typeEmbd and posEmbd based on the result of trigger word recognition; 3. Use distinct CRF layers for each event type to predict arguments and argument roles.

### parameters

python DataLoadAndTrain.py --LOSS_alpha=1 --lr=1e-5 --l2=1e-5 --early_stop=5 --PreTrain_Model="XLMRoberta_large" --batch_size=16

### results
[trigger classification]    P=0.685    R=0.717    F1=0.701  
[argument classification]    P=0.413    R=0.256    F1=0.316  
[trigger identification]    P=0.738    R=0.772    F1=0.755  
[argument identification]    P=0.457    R=0.283    F1=0.349  

