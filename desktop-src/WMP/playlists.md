---
title: Списки воспроизведения
description: Списки воспроизведения
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Проигрыватель Windows Media, списки воспроизведения
- Объектная модель проигрывателя Windows Media, списки воспроизведения
- Объектная модель, списки воспроизведения
- Элемент управления ActiveX проигрывателя Windows Media, списки воспроизведения
- Элементы управления ActiveX, списки воспроизведения
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, списки воспроизведения
- Проигрыватель Windows Media Mobile, списки воспроизведения
- списки воспроизведения, миграция
- Списки воспроизведения метафайлов Windows Media, миграция
- списки воспроизведения метафайлов, миграция
- рекомендации по миграции, списки воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124c07a6bd3aec0bebd235678e9fa8a5f069ec73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067707"
---
# <a name="playlists"></a>Списки воспроизведения

Объектная модель элемента управления ActiveX проигрывателя Windows Media 6,4 включает четыре метода и одно свойство для работы с списками воспроизведения метафайлов Windows Media.

-   *Player6*. **Жеткуррентентри**
-   *Player6*. **Сеткуррентентри**
-   *Player6*. **Жетмедиапараметер**
-   *Player6*. **Жетмедиапараметернаме**
-   *Player6*. **Ентрикаунт**.

Вместе они предоставляют ограниченную функциональность для навигации по метафайлу списка воспроизведения с расширением файла. ASX и получением сведений о записях, содержащихся в списке воспроизведения.

Проигрыватель Windows Media 7 представил «библиотеку мультимедиа». Библиотека позволяет пользователям упорядочивать мультимедийное содержимое, а также создавать пользовательские списки воспроизведения, которыми можно управлять с помощью графического пользовательского интерфейса проигрывателя. Объектная модель элементов управления ActiveX проигрывателя Windows Media 7 или более поздней версии обеспечивает поддержку работы с списками воспроизведения библиотек, а также списков воспроизведения, содержащихся в метафайлах Windows Media, с расширением файла. ASX.

> [!Note]  
> По соображениям безопасности пользователь должен предоставить доступ к библиотеке, прежде чем программа сможет манипулировать ее содержимым. Права доступа могут запрашиваться и предоставляться только через объектную модель Windows Media 9 Series или более поздней версии. Дополнительные сведения о правах доступа см. в разделе [доступ к библиотеке](library-access.md).

 

Объектная модель проигрывателя Windows Media 7 или более поздней версии содержит три объекта для обработки списков воспроизведения. Объект **плайлистколлектион** предоставляет функциональные возможности для организации списков воспроизведения. Он представляет всю коллекцию списков воспроизведения в библиотеке пользователя. Объект **плайлистаррай** предоставляет способ получения определенного списка воспроизведения из объекта **плайлистколлектион** с помощью номера индекса. два метода объекта **плайлистколлектион** извлекают объект **плайлистаррай** . Объект **списка воспроизведения** предоставляет свойства и методы, необходимые для управления элементами мультимедиа, содержащимися в одном списке воспроизведения.

Например, поскольку каждый список воспроизведения в библиотеке имеет уникальное имя, список воспроизведения можно получить из библиотеки с помощью *плайлистколлектион*. метод **жетбинаме** :


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



Чаще всего требуется работать с текущим списком воспроизведения. Хотя можно использовать несколько объектов списков воспроизведения, *проигрыватель* может получить только один из них. Свойство **куррентплайлист** в любое заданное время: тот, который проигрыватель Windows Media обрабатывает в данный момент.

Когда проигрыватель Windows Media 7 или более поздней версии воспроизводит метафайл Windows Media с расширением ASX-файла, сначала создается объект **списка воспроизведения** . Затем он заполняет объект данными из списка воспроизведения ASX, после чего объект **списка воспроизведения** становится текущим списком воспроизведения. Это означает, что вы можете использовать свойства и методы, связанные с объектом **списка воспроизведения** , для управления списками воспроизведения ASX точно так же, как вы бы работали с списками воспроизведения в библиотеке. Например, чтобы получить количество записей в списке воспроизведения ASX с помощью объектной модели версии 6,4, используется *Player6*. **Ентрикаунт** , свойство:


```C++
var entrycount = WMP64.EntryCount;

```



При использовании объектной модели проигрывателя Windows Media 7 или более поздней версии используется *список воспроизведения*. Свойство **Count** :


```C++
var entrycount = WMP9.currentPlaylist.count;

```



При использовании элемента управления версии 6,4 можно использовать *Player6*. Метод **жеткуррентентри** для получения индекса текущей записи в списке воспроизведения ASX:


```C++
var entrynum = WMP64.GetCurrentEntry();

```



Тот же результат можно получить с помощью объектной модели проигрывателя Windows Media 7 или более поздней версии в скрипте. В следующем примере JScript сравнивается текущий объект мультимедиа с каждым элементом списка воспроизведения. Когда *носитель*. Функция **IsTrue возвращает значение** true, а в окне сообщения отображается индекс текущего элемента мультимедиа.


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



Чтобы указать индекс текущей записи в списке воспроизведения ASX, используйте *Player6*. **Сеткуррентентри**. Индексы записи списка воспроизведения в версии 6,4 начинаются с 1, поэтому чтобы вторая запись в списке воспроизведения метафайлов была текущей, используйте следующий синтаксис:


```C++
WMP6.SetCurrentEntry(2);

```



Индексы записи списка воспроизведения отсчитываются от нуля в проигрывателе Windows Media 7 или более поздней версии. чтобы сделать вторую запись в списке воспроизведения метафайла текущей, при использовании объектной модели проигрывателя Windows Media 7 или более поздней используйте следующий синтаксис:


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



В следующем примере JScript показана функция, которая принимает номер индекса в качестве параметра, а затем создает запись списка воспроизведения, соответствующую индексу текущего элемента мультимедиа:


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



Метафайлы Windows Media могут содержать настраиваемые элементы параметров, которые задаются с помощью **<PARAM>** тега. При использовании объектной модели версии 6,4 можно получить имя определенного параметра с помощью *Player6*. Метод **жетмедиапараметернаме** . В следующем примере JScript извлекается имя первого параметра в первой записи списка воспроизведения ASX:


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



Аналогичным образом можно получить значение, связанное с параметром, с помощью *Player6*. **Жетмедиапараметер**:


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



В следующем примере JScript используется объектная модель проигрывателя Windows Media 7 или более поздней версии для получения имени и значения параметра из первой записи в списке воспроизведения. asx:


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



Можно использовать *плайлистколлектион*. метод **импортплайлист** для добавления списка воспроизведения ASX в библиотеку. После импорта список воспроизведения метафайлов станет списком воспроизведения библиотеки, чтобы вы могли работать с ним, используя все свойства и методы в процессе реализации. Чтобы приложение могло использовать метод **импортплайлист** , пользователь должен предоставить библиотеке права полного доступа к ней.

Можно использовать *плайлистколлектион*. **жетбинаме** проверить, существует ли список воспроизведения. Этот метод всегда возвращает допустимый объект **плайлистаррай** . Если полученный массив списков воспроизведения содержит только один список воспроизведения, то в библиотеке существует список воспроизведения с таким именем. В противном случае массив списков воспроизведения не будет содержать объект списка воспроизведения. Это означает, что в библиотеке отсутствует список воспроизведения с именем, переданным в качестве аргумента в метод **жетбинаме** . Это показано в следующем примере JScript:


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Управление списками воспроизведения**](managing-playlists.md)
</dt> <dt>

[**Руководством по миграции объектной модели**](object-model-migration-guide.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> </dl>

 

 




