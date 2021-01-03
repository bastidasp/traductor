, 'caserio': 'yataram'
, 'techo de hoja': 'yatkih'
, 'labrar':'yatna'
, 'estoy labrando': 'yatnus'
, 'zocolar': 'yatnus'
, 'cuantos':'yawa'
, 'oruga':'am'
, 'buenos dias':'watkɨnmari'}



def main():
    st.sidebar.header("BIENBENIDO:  AQUI CONOCERAS SOBRE LA LENGUA AWAPIT ")
    
    
    menu= [" Traductor","vocales","abecedario","AWAPIT"]
    choice= st.sidebar.selectbox("Menu", menu)
    if choice == "Traductor":
        st.text("")
             
    
                
    elif choice == "vocales":
        st.subheader("VOCALES")
        if st.button("DE LA LENGUA AWAPIT "):
            image = Image.open('abecedario.jpg') # IMAGEN
            st.image(image, caption='Unidad Indigena Del Pueblo Awa UNIPA',use_column_width=True)
        else:
            st.text("vocales en awapit")
        
    elif choice == "abecedario":
        st.subheader("ABECEDARIO")
        if st.button("DE LA LENGUA AWAPIT"):
            imag = Image.open('abec.jpg') # IMAGEN
            st.image(imag,width=800,caption='Unidad Indigena Del Pueblo Awa UNIPA')
        else:
            st.text("abecedario en awapit")

    elif choice == "AWAPIT":
        st.subheader("AWAPIT")
        
        if st.button("LA LENGUA AWAPIT "):
            st.text("""La lengua nativa Awapit suele considerarse aislada, sin ninguna filiación
lingüística; sin embargo, algunos autores la clasifican desde los estudios de
Beuchat & Rivet (1910) y Rivet & Loukotka (1952) dentro de la familia lingüística
barbacoa, junto con las lenguas Tsa’fiki y el Cha’palaa1
 y el Guambiano - Totoró2
(Curnow y Liddicoat (1998: 405), Fabre (2005). No obstante, otros lingüistas la han
emparentado con la familia macro-chibcha (Ministerio de Cultura de Colombia).
Varios estudios comparativos del vocabulario de estas lenguas establecen un
parentesco más cercano entre el Tsa’fiki y el Cha’palaa que entre estas dos
lenguas y el Awapit. Swadesh, calcula que las lenguas del grupo barbacoa se
separaron para constituirse en entidades lingüísticas independientes desde
hace más de 33 siglos (Swadesh 1959), y que el Awa pit es precisamente la
más diferenciada del grupo.
El Awa pit es, en resumen, no sólo una lengua amenazada _como la mayoría de
las lenguas ancestrales de nuestro país _, sino además una lengua altamente
vulnerable, es decir, aquella cuyos hablantes se encuentran en condiciones
sociales, políticas y económicas desfavorables en comparación con otros
colectivos lingüísticos (Gómez Rendón, J. 2010)""")
        else:
            st.text("SI TE INTERESA CONOCER UN POCO MAS SOBRE EL AWAPIT DALE click")
            
            
            

st.title("TRADUCTOR ESPAÑOL AWAPIT")

st.markdown("**caracteres que te permitira escribir y buscar en awapit**")
st.write (  'ã     ĩ    ɨ    ũ')

a= st.radio("seleccione la lengua",["AWAPIT","ESPAÑOL"])  # permite elegir la lengua 

        
# permite elegir la lengua a traducir 
if st.button("Buscar"):
    st.text("")

    #with st.spinner("Buscando..."):
        #time.sleep(1)
    
elif a == "AWAPIT": 
    palabra=st.text_input("ingrese la palabra en awapit")
    x=palabra.lower()
    if palabra != "AWAPIT":
        Traduccion=div[x]   # buscamos en el diccionario   div la clave  
        st.text(f"La traduccion es : {Traduccion}")
    else:
        st.text("no esta definido")
        
         
if a == "ESPAÑOL":
    palabra=st.text_input("ingrese la palabra en español")
    x=palabra.lower()
    if palabra != "ESPAÑOL":
        Traduccion=dicc[x]
        x=st.write(f"La traduccion es : {Traduccion}")   
            

        
            
       
        
if __name__=='__main__':
    main()
