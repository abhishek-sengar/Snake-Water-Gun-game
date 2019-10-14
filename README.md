# Snake-Water-Gun-game
import random
c=0
p=0
for i in range(5):
	a=random.choice(['s','w','g'])
	n=input('Enter s: snake w: water g: gun\n')
	if(n=='s' or n=='w' or n=='g'):
		if(a=='s'):
			if(n=='g'):
				print('You Won  ','cpu choice ',a)
				p=p+10
			elif(n=='w'):
				print('You Lose ','cpu choice ',a)
				c=c+10
			else:
				print('Tie      ','cpu choice ',a)
		elif(a=='w'):
			if(n=='s'):
				print('You Won  ','cpu choice ',a)
				p=p+10
			elif(n=='g'):
				print('You Lose ','cpu choice ',a)
				c=c+10
			else:
				print('Tie      ','cpu choice ',a)
		else:
			if(n=='w'):
				print('You Won  ','cpu choice ',a)
				p=p+10
			elif(n=='s'):
				print('You Lose ','cpu choice ',a)
				c=c+10
			else:
				print('Tie      ','cpu choice ',a)
	else:
		i=i-1
		print('Enter Valid Input')
			
print('Your Final Score ',p)
print('cpu final score ',c)
if(p>c):
	print('You won this series by',p-c,' points')
elif(p<c):
	print('You lose this series by',c-p,' points')
else:
	print('Series Tie')
