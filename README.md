Processo de instalação do React Navigation em um projeto React Native:

1. Instalação:
  yarn add @react-navigation/native
2. Instalando dependência em um Projeto criado com Expo:
expo install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context @react-native-community/masked-view
3. Instalando Stack Navigation para navegar entre telas
yarn add @react-navigation/stack
4. (Opcional) Instalando Drawer Navigation para ter um menu lateral deslizante
yarn add @react-navigation/drawer
5. Importar no seu projeto React Native:
import { NavigationContainer } from '@react-navigation/native'; //Fundamental
import { createStackNavigator } from '@react-navigation/stack'; //Navegação entre telas
import { createDrawerNavigator } from '@react-navigation/drawer'; //Para Drawer

Como usar:
Depois de importar tudo que for necessário, você deve definir que tipo de navegação pretende ter. Se quiser ter uma navegação a partir de botões no seu app faça:
const Stack = createStackNavigator();
function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator initialRouteName="Home">
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Details" component={DetailsScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}
Assim, você terá algo como:
navigation
