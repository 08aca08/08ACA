# 08ACA
HIHG
import matplotlib.pyplot as plt

# Dades dels percentatges per a cada caràcter
caracters = ['Color dels cabells', 'Color dels ulls', 'Clotet a la barbeta', 'Enrotllament de la llengua', 'Forma de plegar els braços']
percentatges_dominants = [58.82, 70.37, 4.76, 81.48, 57.14]
percentatges_recessius = [41.18, 29.63, 95.24, 18.52, 42.86]

# Colors per als sectors (opcional)
colors = ['#ff9999','#66b3ff','#99ff99','#ffcc99', '#c2c2f0']

# Creació dels gràfics
fig, axs = plt.subplots(2, 3, figsize=(15, 10))

# Creació dels gràfics per a cada caràcter
for i, ax in enumerate(axs.flat):
    ax.pie([percentatges_dominants[i], percentatges_recessius[i]], labels=['Dominant', 'Recessiu'], colors=colors, autopct='%1.1f%%', startangle=140)
    ax.set_title(caracters[i])

# Ajustament de l'espai entre subgràfics
plt.tight_layout()

# Mostra dels gràfics
plt.show()
