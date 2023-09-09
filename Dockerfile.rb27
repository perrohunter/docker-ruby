# Usar la imagen oficial de Ruby
FROM ruby:2.7

# Instalar dependencias
RUN apt-get update -qq && apt-get install -y build-essential

# Crear un directorio para la aplicación
WORKDIR /usr/src/app

# Copiar el Gemfile y Gemfile.lock al contenedor
COPY Gemfile* ./

# Instalar las gemas
RUN bundle install

# Copiar el resto de la aplicación al contenedor
COPY . .

# Exponer el puerto 4567
EXPOSE 4567

# Comando para iniciar la aplicación
CMD ["ruby", "app.rb", "-o", "0.0.0.0"]
