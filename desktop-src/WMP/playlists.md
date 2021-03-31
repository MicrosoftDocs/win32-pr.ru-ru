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
# <a name="playlists"></a><span data-ttu-id="628d6-114">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="628d6-114">Playlists</span></span>

<span data-ttu-id="628d6-115">Объектная модель элемента управления ActiveX проигрывателя Windows Media 6,4 включает четыре метода и одно свойство для работы с списками воспроизведения метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="628d6-115">The Windows Media Player 6.4 ActiveX control object model includes four methods and one property for working with Windows Media metafile playlists:</span></span>

-   <span data-ttu-id="628d6-116">*Player6*. **Жеткуррентентри**</span><span class="sxs-lookup"><span data-stu-id="628d6-116">*Player6*.**GetCurrentEntry**</span></span>
-   <span data-ttu-id="628d6-117">*Player6*. **Сеткуррентентри**</span><span class="sxs-lookup"><span data-stu-id="628d6-117">*Player6*.**SetCurrentEntry**</span></span>
-   <span data-ttu-id="628d6-118">*Player6*. **Жетмедиапараметер**</span><span class="sxs-lookup"><span data-stu-id="628d6-118">*Player6*.**GetMediaParameter**</span></span>
-   <span data-ttu-id="628d6-119">*Player6*. **Жетмедиапараметернаме**</span><span class="sxs-lookup"><span data-stu-id="628d6-119">*Player6*.**GetMediaParameterName**</span></span>
-   <span data-ttu-id="628d6-120">*Player6*. **Ентрикаунт**.</span><span class="sxs-lookup"><span data-stu-id="628d6-120">*Player6*.**EntryCount**.</span></span>

<span data-ttu-id="628d6-121">Вместе они предоставляют ограниченную функциональность для навигации по метафайлу списка воспроизведения с расширением файла. ASX и получением сведений о записях, содержащихся в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="628d6-121">Together, these provide limited functionality for navigating a playlist metafile with an .asx file name extension and retrieving information about the entries contained in the playlist.</span></span>

<span data-ttu-id="628d6-122">Проигрыватель Windows Media 7 представил «библиотеку мультимедиа».</span><span class="sxs-lookup"><span data-stu-id="628d6-122">Windows Media Player 7 introduced "Media Library."</span></span> <span data-ttu-id="628d6-123">Библиотека позволяет пользователям упорядочивать мультимедийное содержимое, а также создавать пользовательские списки воспроизведения, которыми можно управлять с помощью графического пользовательского интерфейса проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="628d6-123">The library allows users to organize their digital media content, as well as to create custom playlists that can be managed from the Player graphical user interface.</span></span> <span data-ttu-id="628d6-124">Объектная модель элементов управления ActiveX проигрывателя Windows Media 7 или более поздней версии обеспечивает поддержку работы с списками воспроизведения библиотек, а также списков воспроизведения, содержащихся в метафайлах Windows Media, с расширением файла. ASX.</span><span class="sxs-lookup"><span data-stu-id="628d6-124">The Windows Media Player 7 or later ActiveX control object model provides support for working with library playlists, as well as playlists contained in Windows Media metafiles with an .asx file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="628d6-125">По соображениям безопасности пользователь должен предоставить доступ к библиотеке, прежде чем программа сможет манипулировать ее содержимым.</span><span class="sxs-lookup"><span data-stu-id="628d6-125">For security reasons, the user must grant access rights to the library before your program can manipulate its content.</span></span> <span data-ttu-id="628d6-126">Права доступа могут запрашиваться и предоставляться только через объектную модель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="628d6-126">Access rights can only be requested and granted through the Windows Media Player 9 Series or later object model.</span></span> <span data-ttu-id="628d6-127">Дополнительные сведения о правах доступа см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="628d6-127">For details about access rights, see [Library Access](library-access.md).</span></span>

 

<span data-ttu-id="628d6-128">Объектная модель проигрывателя Windows Media 7 или более поздней версии содержит три объекта для обработки списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="628d6-128">The Windows Media Player 7 or later object model includes three objects for handling playlists.</span></span> <span data-ttu-id="628d6-129">Объект **плайлистколлектион** предоставляет функциональные возможности для организации списков воспроизведения. Он представляет всю коллекцию списков воспроизведения в библиотеке пользователя.</span><span class="sxs-lookup"><span data-stu-id="628d6-129">The **PlaylistCollection** object provides functionality for organizing playlists; it represents the entire collection of playlists in the user's library.</span></span> <span data-ttu-id="628d6-130">Объект **плайлистаррай** предоставляет способ получения определенного списка воспроизведения из объекта **плайлистколлектион** с помощью номера индекса. два метода объекта **плайлистколлектион** извлекают объект **плайлистаррай** .</span><span class="sxs-lookup"><span data-stu-id="628d6-130">The **PlaylistArray** object provides a way to retrieve a specific playlist from the **PlaylistCollection** object by using an index number; two of the **PlaylistCollection** object methods retrieve a **PlaylistArray** object.</span></span> <span data-ttu-id="628d6-131">Объект **списка воспроизведения** предоставляет свойства и методы, необходимые для управления элементами мультимедиа, содержащимися в одном списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="628d6-131">The **Playlist** object provides the properties and methods necessary to manipulate media items contained in a single playlist.</span></span>

<span data-ttu-id="628d6-132">Например, поскольку каждый список воспроизведения в библиотеке имеет уникальное имя, список воспроизведения можно получить из библиотеки с помощью *плайлистколлектион*. метод **жетбинаме** :</span><span class="sxs-lookup"><span data-stu-id="628d6-132">As an example, since each playlist in the library has a unique name, you can retrieve a playlist from the library using the *PlaylistCollection*.**getByName** method:</span></span>


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



<span data-ttu-id="628d6-133">Чаще всего требуется работать с текущим списком воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="628d6-133">You will most frequently want to work with the current playlist.</span></span> <span data-ttu-id="628d6-134">Хотя можно использовать несколько объектов списков воспроизведения, *проигрыватель* может получить только один из них. Свойство **куррентплайлист** в любое заданное время: тот, который проигрыватель Windows Media обрабатывает в данный момент.</span><span class="sxs-lookup"><span data-stu-id="628d6-134">While it is possible to use several playlist objects, only one can be retrieved by the *Player*.**currentPlaylist** property at any given time: the one that Windows Media Player is processing at that moment.</span></span>

<span data-ttu-id="628d6-135">Когда проигрыватель Windows Media 7 или более поздней версии воспроизводит метафайл Windows Media с расширением ASX-файла, сначала создается объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="628d6-135">When Windows Media Player 7 or later plays a Windows Media metafile with an .asx file name extension, it first creates a **Playlist** object.</span></span> <span data-ttu-id="628d6-136">Затем он заполняет объект данными из списка воспроизведения ASX, после чего объект **списка воспроизведения** становится текущим списком воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="628d6-136">Next, it fills the object with the information from the .asx playlist, and then makes that **Playlist** object the current playlist.</span></span> <span data-ttu-id="628d6-137">Это означает, что вы можете использовать свойства и методы, связанные с объектом **списка воспроизведения** , для управления списками воспроизведения ASX точно так же, как вы бы работали с списками воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="628d6-137">This means that you can use the properties and methods associated with the **Playlist** object to manipulate .asx playlists exactly as you would handle playlists in the library.</span></span> <span data-ttu-id="628d6-138">Например, чтобы получить количество записей в списке воспроизведения ASX с помощью объектной модели версии 6,4, используется *Player6*. **Ентрикаунт** , свойство:</span><span class="sxs-lookup"><span data-stu-id="628d6-138">For instance, to retrieve the number of entries in an .asx playlist using the version 6.4 object model, you use the *Player6*.**EntryCount** property:</span></span>


```C++
var entrycount = WMP64.EntryCount;

```



<span data-ttu-id="628d6-139">При использовании объектной модели проигрывателя Windows Media 7 или более поздней версии используется *список воспроизведения*. Свойство **Count** :</span><span class="sxs-lookup"><span data-stu-id="628d6-139">When using the Windows Media Player 7 or later object model, you use the *Playlist*.**count** property:</span></span>


```C++
var entrycount = WMP9.currentPlaylist.count;

```



<span data-ttu-id="628d6-140">При использовании элемента управления версии 6,4 можно использовать *Player6*. Метод **жеткуррентентри** для получения индекса текущей записи в списке воспроизведения ASX:</span><span class="sxs-lookup"><span data-stu-id="628d6-140">When using the version 6.4 control, you can use the *Player6*.**GetCurrentEntry** method to retrieve the index of the current entry in an .asx playlist:</span></span>


```C++
var entrynum = WMP64.GetCurrentEntry();

```



<span data-ttu-id="628d6-141">Тот же результат можно получить с помощью объектной модели проигрывателя Windows Media 7 или более поздней версии в скрипте.</span><span class="sxs-lookup"><span data-stu-id="628d6-141">You can achieve the same result by using the Windows Media Player 7 or later object model in script.</span></span> <span data-ttu-id="628d6-142">В следующем примере JScript сравнивается текущий объект мультимедиа с каждым элементом списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="628d6-142">The following JScript example compares the current media object to each item in the playlist.</span></span> <span data-ttu-id="628d6-143">Когда *носитель*. Функция **IsTrue возвращает значение** true, а в окне сообщения отображается индекс текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="628d6-143">When *Media*.**isIdentical** returns true, a message box displays the index of the current media item.</span></span>


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



<span data-ttu-id="628d6-144">Чтобы указать индекс текущей записи в списке воспроизведения ASX, используйте *Player6*. **Сеткуррентентри**.</span><span class="sxs-lookup"><span data-stu-id="628d6-144">To specify the index of the current entry in an .asx playlist, you use *Player6*.**SetCurrentEntry**.</span></span> <span data-ttu-id="628d6-145">Индексы записи списка воспроизведения в версии 6,4 начинаются с 1, поэтому чтобы вторая запись в списке воспроизведения метафайлов была текущей, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="628d6-145">Playlist entry indexes in version 6.4 start with 1, so to make the second entry in a metafile playlist the current one, use the following syntax:</span></span>


```C++
WMP6.SetCurrentEntry(2);

```



<span data-ttu-id="628d6-146">Индексы записи списка воспроизведения отсчитываются от нуля в проигрывателе Windows Media 7 или более поздней версии. чтобы сделать вторую запись в списке воспроизведения метафайла текущей, при использовании объектной модели проигрывателя Windows Media 7 или более поздней используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="628d6-146">Playlist entry indexes are zero-based in Windows Media Player 7 or later; to make the second entry in a metafile playlist the current one, when using the Windows Media Player 7 or later object model, use the following syntax:</span></span>


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



<span data-ttu-id="628d6-147">В следующем примере JScript показана функция, которая принимает номер индекса в качестве параметра, а затем создает запись списка воспроизведения, соответствующую индексу текущего элемента мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="628d6-147">The following JScript example demonstrates a function that accepts an index number as a parameter, and then makes the playlist entry that corresponds to the index the current media item:</span></span>


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



<span data-ttu-id="628d6-148">Метафайлы Windows Media могут содержать настраиваемые элементы параметров, которые задаются с помощью **<PARAM>** тега.</span><span class="sxs-lookup"><span data-stu-id="628d6-148">Windows Media metafiles can contain custom parameter elements, which you specify by using the **<PARAM>** tag.</span></span> <span data-ttu-id="628d6-149">При использовании объектной модели версии 6,4 можно получить имя определенного параметра с помощью *Player6*. Метод **жетмедиапараметернаме** .</span><span class="sxs-lookup"><span data-stu-id="628d6-149">When using the version 6.4 object model, you can retrieve the name of a particular parameter with the *Player6*.**GetMediaParameterName** method.</span></span> <span data-ttu-id="628d6-150">В следующем примере JScript извлекается имя первого параметра в первой записи списка воспроизведения ASX:</span><span class="sxs-lookup"><span data-stu-id="628d6-150">The following JScript example retrieves the name of the first parameter in the first entry of an .asx playlist:</span></span>


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



<span data-ttu-id="628d6-151">Аналогичным образом можно получить значение, связанное с параметром, с помощью *Player6*. **Жетмедиапараметер**:</span><span class="sxs-lookup"><span data-stu-id="628d6-151">Similarly, you can retrieve the value associated with the parameter using *Player6*.**GetMediaParameter**:</span></span>


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



<span data-ttu-id="628d6-152">В следующем примере JScript используется объектная модель проигрывателя Windows Media 7 или более поздней версии для получения имени и значения параметра из первой записи в списке воспроизведения. asx:</span><span class="sxs-lookup"><span data-stu-id="628d6-152">The following JScript example uses the Windows Media Player 7 or later object model to retrieve the parameter name and value from the first entry in an .asx playlist:</span></span>


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



<span data-ttu-id="628d6-153">Можно использовать *плайлистколлектион*. метод **импортплайлист** для добавления списка воспроизведения ASX в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="628d6-153">You can use the *PlaylistCollection*.**importPlaylist** method to add an .asx playlist to the library.</span></span> <span data-ttu-id="628d6-154">После импорта список воспроизведения метафайлов станет списком воспроизведения библиотеки, чтобы вы могли работать с ним, используя все свойства и методы в процессе реализации.</span><span class="sxs-lookup"><span data-stu-id="628d6-154">Once imported, the metafile playlist becomes a library playlist, so you can manipulate it using all the properties and methods at your disposal.</span></span> <span data-ttu-id="628d6-155">Чтобы приложение могло использовать метод **импортплайлист** , пользователь должен предоставить библиотеке права полного доступа к ней.</span><span class="sxs-lookup"><span data-stu-id="628d6-155">The user must grant full access rights to the library for your application to be able to use the **importPlaylist** method.</span></span>

<span data-ttu-id="628d6-156">Можно использовать *плайлистколлектион*. **жетбинаме** проверить, существует ли список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="628d6-156">You can use *PlaylistCollection*.**getByName** to test whether a playlist exists.</span></span> <span data-ttu-id="628d6-157">Этот метод всегда возвращает допустимый объект **плайлистаррай** .</span><span class="sxs-lookup"><span data-stu-id="628d6-157">This method always returns a valid **PlaylistArray** object.</span></span> <span data-ttu-id="628d6-158">Если полученный массив списков воспроизведения содержит только один список воспроизведения, то в библиотеке существует список воспроизведения с таким именем.</span><span class="sxs-lookup"><span data-stu-id="628d6-158">If the playlist array retrieved contains exactly one playlist, then there exists a playlist with that name in the library.</span></span> <span data-ttu-id="628d6-159">В противном случае массив списков воспроизведения не будет содержать объект списка воспроизведения. Это означает, что в библиотеке отсутствует список воспроизведения с именем, переданным в качестве аргумента в метод **жетбинаме** .</span><span class="sxs-lookup"><span data-stu-id="628d6-159">Otherwise, the playlist array will contain no playlist object; this means there is no playlist in the library with the name passed as an argument to the **getByName** method.</span></span> <span data-ttu-id="628d6-160">Это показано в следующем примере JScript:</span><span class="sxs-lookup"><span data-stu-id="628d6-160">The following JScript example demonstrates this:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="628d6-161">См. также</span><span class="sxs-lookup"><span data-stu-id="628d6-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="628d6-162">**Управление списками воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="628d6-162">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="628d6-163">**Руководством по миграции объектной модели**</span><span class="sxs-lookup"><span data-stu-id="628d6-163">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="628d6-164">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="628d6-164">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




