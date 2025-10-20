def obter_primeiro_elemento(lista):
    2   """
    3   Retorna o primeiro elemento de uma lista.
    4   """
    5   # Passo 1: Acessar o elemento no índice 0 da lista.
    6   # Esta é uma operação de tempo constante.
    7   if lista:
    8     return lista[0]
    9   return None
   10
   11 # --- Análise de Complexidade ---
   12 # Complexidade Temporal: O(1)
   13 # A função executa um número fixo de operações, independentemente do tamanho da lista.
   14
   15 # Complexidade Espacial: O(1)
   16 # A memória utilizada não escala com o tamanho da entrada.
   17
   18 # --- Exemplo de Uso ---
   19 minha_lista = [100, 200, 300]
   20 primeiro_elemento = obter_primeiro_elemento(minha_lista)
   21 print(f"Lista de entrada: {minha_lista}")
   22 print(f"Saída: O primeiro elemento é {primeiro_elemento}")
   23 print("-" * 20)
   24
   25 lista_vazia = []
   26 primeiro_elemento = obter_primeiro_elemento(lista_vazia)
   27 print(f"Lista de entrada: {lista_vazia}")
   28 print(f"Saída: A lista está vazia, retornou {primeiro_elemento}")
   29
   30 # --- Saída Esperada ---
   31 # Lista de entrada: [100, 200, 300]
   32 # Saída: O primeiro elemento é 100
   33 # --------------------
   34 # Lista de entrada: []
   35 # Saída: A lista está vazia, retornou None



   def encontrar_soma_total(lista):
    2   """
    3   Calcula a soma de todos os números em uma lista.
    4   """
    5   # Passo 1: Inicializar uma variável para armazenar a soma.
    6   soma_total = 0
    7
    8   # Passo 2: Iterar sobre cada elemento da lista.
    9   # O loop será executado 'n' vezes, onde 'n' é o número de elementos.
   10   for numero in lista:
   11     # Passo 3: Adicionar o elemento atual à soma total.
   12     soma_total += numero
   13
   14   # Passo 4: Retornar a soma final.
   15   return soma_total
   16
   17 # --- Análise de Complexidade ---
   18 # Complexidade Temporal: O(n)
   19 # O tempo de execução é diretamente proporcional ao número de elementos (n) na lista.
   20
   21 # Complexidade Espacial: O(1)
   22 # A memória extra utilizada (para a variável 'soma_total') é constante.
   23
   24 # --- Exemplo de Uso ---
   25 minha_lista = [10, 20, 30, 40]
   26 soma = encontrar_soma_total(minha_lista)
   27 print(f"Lista de entrada: {minha_lista}")
   28 print(f"Saída: A soma total é {soma}")
   29
   30 # --- Saída Esperada ---
   31 # Lista de entrada: [10, 20, 30, 40]
   32 # Saída: A soma total é 100



    def possui_pares_com_soma_zero(lista):
    2   """
    3   Verifica se há um par de números na lista cuja soma é zero.
    4   """
    5   n = len(lista)
    6   # Passo 1: O primeiro loop itera do primeiro ao último elemento.
    7   for i in range(n):
    8     # Passo 2: O segundo loop itera do elemento seguinte (i + 1) ao último.
    9     # Isso evita comparar um elemento com ele mesmo e repetir pares.
   10     for j in range(i + 1, n):
   11       # Passo 3: Verifica se a soma do par de elementos é zero.
   12       if lista[i] + lista[j] == 0:
   13         # Se encontrarmos um par, retornamos True imediatamente.
   14         print(f"Par encontrado: ({lista[i]}, {lista[j]})")
   15         return True
   16
   17   # Passo 4: Se os loops terminarem sem encontrar pares, retorna False.
   18   return False
   19
   20 # --- Análise de Complexidade ---
   21 # Complexidade Temporal: O(n²)
   22 # Devido aos dois loops aninhados, o número de operações é proporcional a n².
   23
   24 # Complexidade Espacial: O(1)
   25 # A memória extra utilizada é constante (variáveis de controle dos loops).
   26
   27 # --- Exemplo de Uso ---
   28 lista_com_par = [2, -3, 1, 10, -2, 5]
   29 resultado = possui_pares_com_soma_zero(lista_com_par)
   30 print(f"Lista de entrada: {lista_com_par}")
   31 print(f"Saída: Possui par com soma zero? {resultado}")
   32 print("-" * 20)
   33
   34 lista_sem_par = [1, 2, 3, 4, 5]
   35 resultado = possui_pares_com_soma_zero(lista_sem_par)
   36 print(f"Lista de entrada: {lista_sem_par}")
   37 print(f"Saída: Possui par com soma zero? {resultado}")
   38
   39
   40 # --- Saída Esperada ---
   41 # Par encontrado: (2, -2)
   42 # Lista de entrada: [2, -3, 1, 10, -2, 5]
   43 # Saída: Possui par com soma zero? True
   44 # --------------------
   45 # Lista de entrada: [1, 2, 3, 4, 5]
   46 # Saída: Possui par com soma zero? False
