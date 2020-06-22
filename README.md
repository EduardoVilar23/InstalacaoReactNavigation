# Processo de instalação do React Navigation em um projeto React Native:

React Navigation permite navegação entre telas e mais.

## Instalação
Instalando
```bash
yarn add @react-navigation/native
```
2. Instalando dependências em um Projeto criado com Expo:
```bash
expo install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context @react-native-community/masked-view
```
3. Instalando Stack Navigation para navegar entre telas:
```bash
yarn add @react-navigation/stack
```
4. (Opcional) Instalando Drawer Navigation para ter um menu lateral deslizante:
```bash
yarn add @react-navigation/drawer
```


## Imports

```js
import { NavigationContainer } from '@react-navigation/native'; //Fundamental
```
```js
import { createStackNavigator } from '@react-navigation/stack'; //Navegação entre telas
```
```js
import { createDrawerNavigator } from '@react-navigation/drawer'; //Para Drawer
```

## Uso
Depois de importar tudo que for necessário, você deve definir que tipo de navegação pretende ter. Se quiser ter uma navegação a partir de botões no seu app faça:
*Estas funções podem ser disparadas a partir de qualquer ação.
```js
function HomeScreen({ navigation }) {
  return (
    <View style={{ flex: 1, alignItems: 'center', justifyContent: 'center' }}>
      <Text>Tela Home</Text>
      <Button
        title="Ir para detalhes"
        onPress={() => 
        navigation.navigate('Detalhes')}
      />
    </View>
  );
}
```

Go back:

```react
<Text onPress={() => navigation.goBack() }
   Voltar para home
</Text>
```

Criado por Eduardo Vilar
