# Wilcard_Mask

def wildcard_mask(netmask):
    # La mascara digitada deve ser tipo string (no una direccion ipv4)
	netmask = str(netmask)
    # Romper la entrada a una lista of octetos como integros
	netmask_list = map(int, netmask.split("."))
    #Utilizamos 'XOR' para convertir cada octeto de la mascara
	wildcard_list = [ 255^octec for octec in netmask_list ]
	wildcard_mask = ".".join(map(str,wildcard_list))
	return wildcard_mask

wildcard_mask(str(input("Digite la mascara a convertir ")))
