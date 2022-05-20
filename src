import React from 'react';
import {
  View, 
  Text, 
  StyleSheet, 
  SafeAreaView, 
  StatusBar, 
  Image, 
  Pressable,
  Linking,
} from 'react-native';

const colorGithub = '#1C1C1C';
const imgProfileGithub = 'https://avatars.githubusercontent.com/u/77978576?v=4';
const urlToMyGithub = 'https://github.com/AmandaLimaLuiz';

const App = () => {

  const handlePressGoToGithub = async () => {
    const res = await Linking.canOpenURL(urlToMyGithub);
    if(res){
      await Linking.openURL(urlToMyGithub);
    }
  }
  return (
    <SafeAreaView style={style.container}>
      <StatusBar backgroundColor={colorGithub} barStyle={'light-content'}></StatusBar>
      <View style={style.content}>
        <Image 
        accessibilityLabel='foto rosto Amanda com fundo claro '
        style={style.avatar} 
        source={{uri: imgProfileGithub }}></Image>
        <Text 
        accessibilityLabel='Nome: Amanda '
        style={[style.defaultText, style.name]}>Amanda</Text>
        <Text 
        accessibilityLabel='Nickname: AmandaLimaLuiz  '
        style={[style.defaultText, style.nickName]}>AmandaLimaLuiz</Text>
        <Text 
        accessibilityLabel='description: Software engineer student | Web developer '
        style={[style.defaultText, style.description]}>Software engineer student | Web developer</Text>
        <Pressable onPress={handlePressGoToGithub}>
          <View style={style.buttom}>
          <Text style={style.textButtom}>Open in Github</Text>
          </View>
        </Pressable>        
      </View>
    </SafeAreaView>
  );
};

export default App;

const style = StyleSheet.create({
  container: {
    backgroundColor: colorGithub,
    flex: 1,
    justifyContent: 'center'
  },
  content:{
    alignItems: 'center',
    padding: 10,
  },
  avatar:{
    height: 200,
    width: 200,
    borderRadius: 100,
    borderColor: 'pink',
    borderWidth: 2,
  },
  defaultText:{
    color: 'pink',
  },
  name:{
    marginTop: 20,
    fontSize: 25,
    fontWeight: 'bold',
  },
  nickName:{
    fontSize: 16,
    color: '#8B6969'
  },
  description:{
    fontSize: 16,
    fontWeight: 'bold',
  },
 buttom:{
  backgroundColor: '#8B6969',
  borderRadius: 15,
  padding: 18,
  marginTop: 35,
 },
 textButtom:{
  fontSize: 14,
  fontWeight: 'bold',
  color: colorGithub,
 },
});
