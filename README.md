class Macaco:
    def __init__(self, nome):
        self.nome = nome
        self.bucho = []

    def comer(self, alimento):
        self.bucho.append(alimento)

    def verBucho(self):
        if self.bucho:
            print(f"Bucho do macaco {self.nome}: {', '.join(self.bucho)}")
        else:
            print(f"Bucho do macaco {self.nome} está vazio.")

    def digerir(self):
        if self.bucho:
            print(f"Macaco {self.nome} está digerindo...")
            self.bucho = []
        else:
            print(f"Bucho do macaco {self.nome} já está vazio.")


# Teste interativo
macaco1 = Macaco("Mico")
macaco2 = Macaco("Giba")

# Alimentando os macacos
macaco1.comer("Banana")
macaco1.comer("Maçã")
macaco1.comer("Laranja")
macaco2.comer("Abacaxi")
macaco2.comer("Uva")
macaco2.comer("Pêssego")

# Verificando o conteúdo do estômago
macaco1.verBucho()
macaco2.verBucho()

# Digerindo
macaco1.digerir()
macaco2.digerir()

# Verificando o conteúdo do estômago após a digestão
macaco1.verBucho()
macaco2.verBucho()
