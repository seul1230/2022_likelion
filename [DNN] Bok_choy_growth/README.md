# Bok_choy_growth

2022 likelion ais7 Mini Project 5

### π« Team
μ€9μ€9 - μ‘°μμ¬, κΉμμ§, μ΄μ μ, μμ’μ°, κΆνμ€



<br/>

## π₯¬ Prediction of bok choy growth π₯¬
<p align='center'><img src='https://user-images.githubusercontent.com/72390138/205493584-af95700c-c420-4f95-a5fc-d1c05bb27bc7.png'></p>   

dacon AI κ²½μ§λν : **μ²­κ²½μ± μ±μ₯λ₯  μμΈ‘νκΈ°**                    
μ£Όμ : [https://dacon.io/competitions/official/235961/overview/description](https://dacon.io/competitions/official/235961/overview/description)        
  
π notion : https://www.notion.so/MINI5-AI-b031d68247e24a30b192b24c522284d1

<br/>
  
### π summary     
<p align='center'><img src="https://user-images.githubusercontent.com/72390138/205493735-e21c9908-44e8-45e9-8a9c-f3942f203fa7.png" weight="350" height="350"></p>    

4μ°¨ μ°μνλͺ μλλ₯Ό λ§μ λμ λΆμΌμμλ AI κΈ°μ μ΄ λλ¦¬ μ¬μ©λμ΄ IT κΈ°μ μ λμν μ€λ§νΈν λ± λμ± ν¨μ¨μ μΈ μλ¬Ό μ¬λ°°κ° κ°λ₯ν΄μ§κ³  μμ΅λλ€. μλ¬Όμ ν¨μ¨μ μΈ μμ‘μ μν μ΅μ μ νκ²½μ λμΆνλ€λ©΄ μλ¬Ό μ¬λ°°μ ν° λμμ΄ λ  κ²μ΄λ©°, μ²­κ²½μ± λΏλ§ μλ λͺ¨λ  μλ¬Ό μ¬λ°°μ¨μ΄ μ’μμ§ κ²μλλ€. λ―Έλμ μλ¬Ό μ¬λ°°μμλ μ΄ λ°μ΄ν°λ₯Ό κ°μ§κ³  μΈκ³΅μ§λ₯μ μ΄μ©νμ¬ μλ¬Όλ³ λ§μΆ€ν μλ£¨μμ λμμΈλ€μ΄ νΈλ¦¬νκ³  μΉκ·Όνκ² μν μμμ νμ©νλ μ²« κ±Έμμ λ΄λμ μ μμ κ²μλλ€.      
 
  
λ°λΌμ, **μΈκ³΅μ§λ₯(AI)μ νμ©νμ¬ κ΅­λ΄ κ³ μ  μλ¬Ό μμμμ μ μ©ν μ²μ°λ¬Ό μμ¬λ₯Ό νμνκ³ , κ·Έ ν¨λ₯κ³Ό νμ± λ±μ λν΄ μ°κ΅¬νλ κ²μ΄ λͺ©ν**μλλ€.     
μ€μ  AIλ₯Ό μ΄μ©ν μλ¬Όμ μ¬λ°°νλ μ€λ§νΈνκ³Ό κ°μ κ³³μ μ μ©νκ² μ¬μ©λ  κ²μλλ€.      
  
<br/><br/>
  
### π Data info.     

**dacon μ²­κ²½μ± μμΈ‘ λ°μ΄ν°** : [https://dacon.io/competitions/official/235961/data](https://dacon.io/competitions/official/235961/data) 
[μ²­κ²½μ± μ±μ₯ μμΈ‘ AI κ²½μ§λν](https://dacon.io/competitions/official/235961/data)μμ μ κ³΅λ λ°μ΄ν°λ₯Ό λ€μ΄λ°μ μ΄μ©νμλ€. 

<br/>

**π train input dataset[folder]**   

![image](https://user-images.githubusercontent.com/72390138/205494867-68e0c49a-3740-4fe4-8812-da281ace0524.png)    
μ΄ 58κ° μ²­κ²½μ± μΌμ΄μ€λ₯Ό κ° μ²­κ²½μ± μΌμ΄μ€ λ³ νκ²½ λ°μ΄ν°(1λΆ κ°κ²©)μΌλ‘ κ΅¬μ±λμ΄ μμ      

**π train target dataset[folder]**                  

<img src="https://user-images.githubusercontent.com/72390138/205494955-e4752ba6-3a90-41de-a1ee-ec2929ea8dd6.png" weight="300" height="500">     
μ΄ 58κ° μ²­κ²½μ± μΌμ΄μ€λ₯Ό rate columnμ κ° μ²­κ²½μ± μΌμ΄μ€ λ³ μ λ©΄μ  μ¦κ°λ₯ (1μΌ κ°κ²©)λ‘ κ΅¬μ±λμ΄ μμ       

**π train(input+target) shape**                   
train(input+target) (1813, 43)         
test(input+target) (195, 43)            
  
<br/><br/>
  
### π Visualization
1οΈβ£ λ΄λΆμ¨λκ΄μΈ‘μΉ, λ΄λΆμ΅λκ΄μΈ‘μΉ, μ΄μΆμ κ΄λ, μλ³ rate        
![image](https://user-images.githubusercontent.com/72390138/205497279-d59cb01a-a52e-44f7-9cef-c34381f8fcfd.png)              

<br/>

2οΈβ£ μ μ, μ²­μ, λ°±μ, μ΄μΆ μΆμ κ΄λ λ³ rate
![image](https://user-images.githubusercontent.com/72390138/205497255-0030b727-3f14-4c07-b22b-806a05334616.png)             
λ°±μκ³Ό μ΄μΆλ 100μμ, μ μκ³Ό μ²­μμ 0μμ μ±μ₯λ₯ μ΄ λλ€.     

<br/>
  
3οΈβ£ ECμ CO2μ λλ°©μν       
![image](https://user-images.githubusercontent.com/72390138/205496256-fe545a8c-16b8-4644-a339-030a2d05f271.png)       
ECκ΄μΈ‘μΉκ° ν΄μλ‘ λλ°©μνλ μ μμΌλ©°, λ°λλ‘ μμμλ‘ λλ°©μνλ λμ κ²μ νμΈν  μ μλ€.   

<br/>

4οΈβ£ κ° CASE λ³ μλ©΄μ  μ¦κ°λ₯ (rate) λ³ν      
![image](https://user-images.githubusercontent.com/72390138/205496376-956636fd-c78d-433e-b690-bdb8764cfe71.png)      
λΆν¬λ₯Ό μΌμ νκ² λ§λ€κΈ° μν Scaling κ³Όμ μ΄ νμν¨μ΄ λ³΄μλ€.          
  
 
### π Modeling
π Scaling - RobustScaler      
```python      
from sklearn.preprocessing import RobustScaler        
rb = RobustScaler()         
train_X = rb.fit_transform(train_X)         
test_X = rb.transform(test_X)            
```
  
π Tensorflow    
```python
model = tf.keras.models.Sequential([
    tf.keras.layers.Dense(units=128, input_shape=[input_shape]),
    tf.keras.layers.Dense(128, activation='selu'),
    tf.keras.layers.Dropout(0.1),
    tf.keras.layers.Dense(1)
])
  
optimizer = tf.keras.optimizers.RMSprop(0.001)     
  
model.compile(optimizer=optimizer, 
              loss=["mae", "mse"], 
              metrics=["mae", "mse"])
```

π Pytorch     
```python      
linear1 = torch.nn.Linear(train_X.shape[1], 512, bias=True)
linear3 = torch.nn.Linear(512, 256, bias=True)
linear4 = torch.nn.Linear(256, 128, bias=True)
linear5 = torch.nn.Linear(128, 64, bias=True)
linear6 = torch.nn.Linear(64, 32, bias=True)
linear7 = torch.nn.Linear(32, 10, bias=True)
linear8 = torch.nn.Linear(10, 1, bias=True)

relu = torch.nn.ReLU()
dropout = torch.nn.Dropout(p=0.1)
  
model = torch.nn.Sequential(linear1,relu,
                            linear3,relu,
                            linear4, relu,
                            linear5, relu,
                            linear6, relu,
                            linear7, relu,
                            linear8).to(device)

# nn ν¨ν€μ§λ₯Ό μ¬μ©νμ¬ λͺ¨λΈκ³Ό μμ€ ν¨μλ₯Ό μ μν©λλ€.
loss_fn = torch.nn.MSELoss().to(device)
optimizer = optim.Adam(model.parameters(), lr=0.0005)

# κ°μ€μΉ μ΄κΈ°ν 
torch.nn.init.xavier_normal_(linear1.weight)
torch.nn.init.xavier_normal_(linear2.weight)
torch.nn.init.xavier_normal_(linear3.weight)
torch.nn.init.xavier_normal_(linear4.weight)
torch.nn.init.xavier_normal_(linear5.weight)
torch.nn.init.xavier_normal_(linear6.weight)
torch.nn.init.xavier_normal_(linear7.weight)
torch.nn.init.xavier_normal_(linear8.weight)     
  
Parameter containing:
tensor([[-0.1239,  0.3789, -0.2748,  0.2951,  0.0612,  0.2898,  0.2660, -0.4028,
         -1.1738,  0.6484]], requires_grad=True)        
```

π LSTM    
```python    
class BaseModel(nn.Module):
    def __init__(self):
        super(BaseModel, self).__init__() 
        self.lstm = nn.LSTM(input_size=train_X.shape[1], hidden_size=256, batch_first=True, bidirectional=False) # LSTM λ©λͺ¨λ¦¬ μΆκ° 
        self.dense = nn.Sequential(
            # nn.Linear(256, 10 , torch.nn.ReLU()),
            # Layer μΆκ° 
            nn.Linear(256, 128,  torch.nn.ReLU()),
            nn.Linear(128, 64, torch.nn.ReLU()),
            nn.Linear(64, 32,  torch.nn.ReLU()),
            nn.Linear(32, 10,  torch.nn.ReLU()),
            nn.Linear(10, 1)
        )
        self.dropout = nn.Dropout(0.2)
        
    def forward(self, x):
        hidden, _ = self.lstm(x)
        x = self.dropout(hidden)
        output = self.dense(hidden)
        return output
  
model = BaseModel()
model.eval() 
loss_fn = torch.nn.MSELoss().to(device)
optimizer = optim.Adam(model.parameters(), lr=0.0005)    
```
  
  
### π Submission & Score
πTensorflow      
public : 17.91, private : 17.53    <br/>

π Pytorch    
public : 19.2138, private : 18.009    <br/>

πLSTM      
public : 21.5578 / private 22.5213      <br/>
