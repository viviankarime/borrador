# borrador
# Este código sirve para hacer un primer programa en Streamlit. 
import streamlit as st

# Creamos la lista de páginas
paginas = ['Inicio', '¿Quiénes son María Becerra y Taylor Swift?', 'Descubre tu match musical']

# Creamos botones de navegación tomando la lista de páginas
pagina_seleccionada = st.sidebar.selectbox('Selecciona una página', paginas)

# Generamos condicionales para mostrar el contenido de cada página
if pagina_seleccionada == 'Inicio':

  # Título
  st.markdown("<h1 style='text-align: center;'>print('Blog Mi Experiencia Personal')</h1>", unsafe_allow_html=True)

  # Primer bloque: imagen izquierda, texto derecha
  col1, col2 = st.columns(2)
  col1.image("foto.jpg", caption='La autora inteligente y sexy de este blog', width=300)

  texto = """Aquí va tu texto de presentación, con risas, lágrimas y mucho amor."""
  col2.markdown(f"<div style='text-align: justify; font-size: 15px;'>{texto}</div>", unsafe_allow_html=True)

  # Segundo bloque: texto izquierda, imagen derecha
  col3, col4 = st.columns(2)
  texto2 = """Este es otro espacio para contar algo más sobre tu experiencia o el propósito del blog."""
  col3.markdown(f"<div style='text-align: justify; font-size: 15px;'>{texto2}</div>", unsafe_allow_html=True)
  col4.image("foto2.jpg", caption='La segunda autora igual de fabulosa', width=300)
