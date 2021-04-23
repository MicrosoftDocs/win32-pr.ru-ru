---
title: Метод говорите
description: Метод говорите
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88792a53fac80c68154f938e91fb9bfe63b2b8e3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487624"
---
# <a name="speak-method"></a><span data-ttu-id="9d1b0-103">Метод говорите</span><span class="sxs-lookup"><span data-stu-id="9d1b0-103">Speak Method</span></span>

<span data-ttu-id="9d1b0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9d1b0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9d1b0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="9d1b0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9d1b0-106">Говорит заданный текстовый или звуковой файл для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-106">Speaks the specified text or sound file for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="9d1b0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9d1b0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9d1b0-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Проговаривать* \*  \[ *текст* \] , \[ *URL-адрес*\]</span><span class="sxs-lookup"><span data-stu-id="9d1b0-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speak*\* \[*Text*\], \[*Url*\]</span></span>



| <span data-ttu-id="9d1b0-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="9d1b0-109">Part</span></span>   | <span data-ttu-id="9d1b0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9d1b0-110">Description</span></span>                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d1b0-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="9d1b0-111">*Text*</span></span> | <span data-ttu-id="9d1b0-112">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-112">Optional.</span></span> <span data-ttu-id="9d1b0-113">Строка, указывающая, что сообщает символ.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-113">A string that specifies what the character says.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="9d1b0-114">*Url*</span><span class="sxs-lookup"><span data-stu-id="9d1b0-114">*Url*</span></span>  | <span data-ttu-id="9d1b0-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-115">Optional.</span></span> <span data-ttu-id="9d1b0-116">Строковое выражение, задающее расположение звукового файла (. WAV или. Формат ЛВВ).</span><span class="sxs-lookup"><span data-stu-id="9d1b0-116">A string expression specifying the location of an audio file (.WAV or .LWV format).</span></span> <span data-ttu-id="9d1b0-117">Расположение можно указать в виде файла (включая спецификацию пути UNC) или URL-адреса (если данные анимации символов также извлекаются по протоколу HTTP).</span><span class="sxs-lookup"><span data-stu-id="9d1b0-117">The location can be specified as a file (including a UNC path specification) or URL (when character animation data is also being retrieved via HTTP protocol).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d1b0-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d1b0-118">Remarks</span></span>

<span data-ttu-id="9d1b0-119">Хотя параметры *Text* и *URL* являются необязательными, необходимо указать один из них.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-119">Although the *Text* and *Url* parameters are optional, one of them must be supplied.</span></span> <span data-ttu-id="9d1b0-120">Чтобы использовать этот метод с символом, настроенным для диктовки только в его подсказке или использовании механизма преобразования текста в речь (TTS), просто укажите параметр *Text* .</span><span class="sxs-lookup"><span data-stu-id="9d1b0-120">To use this method with a character configured to speak only in its word balloon or using a text-to-speech (TTS) engine, simply provide the *Text* parameter.</span></span> <span data-ttu-id="9d1b0-121">Включать пробел между словами для определения подходящих слов в тексте всплывающей подсказки, даже для тех языков, которые обычно не содержат пробелов.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-121">Include a space between words to define appropriate word breaks in the word balloon, even for languages that do not traditionally include spaces.</span></span>

<span data-ttu-id="9d1b0-122">Можно также включить в текстовый параметр символы вертикальной черты ( \| ), чтобы назначить альтернативные строки, чтобы сервер случайно выбрал другую строку каждый раз при обработке метода. </span><span class="sxs-lookup"><span data-stu-id="9d1b0-122">You can also include vertical bar characters (\|) in the *Text* parameter to designate alternative strings, so that the server randomly chooses a different string each time it processes the method.</span></span>

<span data-ttu-id="9d1b0-123">Поддержка символов вывода TTS определяется при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-123">Character support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="9d1b0-124">Чтобы создать вывод TTS, перед вызовом этого метода необходимо установить совместимый обработчик TTS.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-124">To generate TTS output, a compatible TTS engine must already be installed before calling this method.</span></span> <span data-ttu-id="9d1b0-125">Дополнительные сведения см. в разделе [доступ к голосовым службам](accessing-speech-services.md).</span><span class="sxs-lookup"><span data-stu-id="9d1b0-125">For further information, see [Accessing Speech Services](accessing-speech-services.md).</span></span>

<span data-ttu-id="9d1b0-126">При использовании записанного звукового файла (. WAV или. Только формат ЛВВ.) выходные данные для символа указывают расположение файла в параметре *URL-адреса* .</span><span class="sxs-lookup"><span data-stu-id="9d1b0-126">If you use recorded sound-file (.WAV or .LWV format only) output for the character, specify the file's location in the *Url* parameter.</span></span> <span data-ttu-id="9d1b0-127">Эта спецификация файла может включать локальный (абсолютный или относительный) или UNC-путь.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-127">This file specification can include a local (absolute or relative) or universal naming convention (UNC) path.</span></span> <span data-ttu-id="9d1b0-128">Имя файла не может содержать символы, не включенные в кодовую страницу США 1252.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-128">The filename cannot include any characters not included in the US code page 1252.</span></span> <span data-ttu-id="9d1b0-129">Однако если для доступа к данным символьной анимации используется протокол HTTP, перед вызовом метода **говорите** используйте метод [**Get**](get-method.md) для загрузки анимации.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-129">However, if you are using the HTTP protocol to access the character animation data, use the [**Get**](get-method.md) method to load the animation before calling the **Speak** method.</span></span> <span data-ttu-id="9d1b0-130">Сведения о творческой работе см. [в разделе Использование средства редактирования лингвистических сведений Майкрософт](using-the-microsoft-linguistic-information-sound-editing-tool.md) . ЛВВ файлы.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-130">See [Using the Microsoft Linguistic Information Sound Editing Tool](using-the-microsoft-linguistic-information-sound-editing-tool.md) for information about creative .LWV files.</span></span>

<span data-ttu-id="9d1b0-131">При использовании записанных выходных данных звукового файла можно по-прежнему использовать параметр Text для указания слов, отображаемых в *тексте* всплывающего слова символа.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-131">When using recorded sound-file output, you can still use the *Text* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="9d1b0-132">Однако при указании лингвистическо расширенного звукового файла (. ЛВВ) для параметра *URL-адреса* и не указывайте текст для всплывающего окна Word, параметр *Text* использует текст, хранящийся в файле.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-132">However, if you specify a linguistically enhanced sound file (.LWV) for the *Url* parameter and do not specify text for the word balloon, the *Text* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="9d1b0-133">Можно также изменять параметры вывода речи специальными тегами, включенными в параметр *Text* .</span><span class="sxs-lookup"><span data-stu-id="9d1b0-133">You can also vary parameters of the speech output with special tags that you include in the *Text* parameter.</span></span> <span data-ttu-id="9d1b0-134">Дополнительные сведения см. в [статье Теги речевого вывода Microsoft Agent](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="9d1b0-134">For more information, see [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

<span data-ttu-id="9d1b0-135">Если объявляется ссылка на объект и устанавливается этот метод, он возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="9d1b0-135">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="9d1b0-136">Его можно использовать для синхронизации других частей кода с выходными данными символа, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="9d1b0-136">You can use this to synchronize other parts of your code with the character's spoken output, as in the following example:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here it is.")
...
   Sub Agent1_RequestComplete (ByVal Request as Object)
   ' Make certain the request exists
   If SpeakRequest Not Nothing Then
      ' See if it was this request
      If Request = SpeakRequest Then
         ' Display the message box 
         Msgbox "Ta da!"
      End If
   End If
   End Sub
```



<span data-ttu-id="9d1b0-137">Можно также использовать объект [**запроса**](/windows/desktop/lwef/the-request-object) для проверки определенных условий возникновения ошибок.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-137">You can also use a [**Request**](/windows/desktop/lwef/the-request-object) object to check for certain error conditions.</span></span> <span data-ttu-id="9d1b0-138">Например, если вы используете метод **говорите** и не установили совместимый механизм TTS, сервер устанавливает свойство [**Status**](status-property.md) объекта **запроса** в значение "Failed" со свойством [**Description**](description-property.md) на "незарегистрированный" класс или ошибка "неизвестный или возвращенный объект".</span><span class="sxs-lookup"><span data-stu-id="9d1b0-138">For example, if you use the **Speak** method to speak and do not have a compatible TTS engine installed, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with its [**Description**](description-property.md) property to "Class not registered" or "Unknown or object returned error".</span></span> <span data-ttu-id="9d1b0-139">Чтобы определить, установлен ли модуль TTS, используйте свойство [**ттсмодеид**](ttsmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="9d1b0-139">To determine if you have a TTS engine installed, use the [**TTSModeID**](ttsmodeid-property.md) property.</span></span>

<span data-ttu-id="9d1b0-140">Аналогичным образом, если вы попытаетесь поговорить с звуковым файлом, а если файл не был загружен или возникла проблема с звуковым устройством, сервер также задает для свойства [**Status**](status-property.md) объекта [**запроса**](/windows/desktop/lwef/the-request-object) значение "сбой" с соответствующим номером кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-140">Similarly, if you have the character attempt to speak a sound file, and if the file has not been loaded or there is a problem with the audio device, the server also sets the [**Request**](/windows/desktop/lwef/the-request-object) object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="9d1b0-141">Для синхронизации кода можно также включить Теги речи в закладки в тексте:</span><span class="sxs-lookup"><span data-stu-id="9d1b0-141">You can also include bookmark speech tags in your Speak text to synchronize your code:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here \mrk=100\it is.")
...
   Sub Agent1_Bookmark (ByVal BookmarkID As Long)
   If BookmarkID = 100 Then
      ' Display the message box 
         Msgbox "Tada!"
      End If
   End Sub
```



<span data-ttu-id="9d1b0-142">Дополнительные сведения о теге распознавания речи см. в разделе [теги вывода речи](mrk-tag.md).</span><span class="sxs-lookup"><span data-stu-id="9d1b0-142">For more information on the bookmark speech tag, see [Speech Output Tags](mrk-tag.md).</span></span>

<span data-ttu-id="9d1b0-143">Метод **говорите** использует последнее действие, чтобы определить, какую анимацию речи следует воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-143">The **Speak** method uses the last action played to determine which speaking animation to play.</span></span> <span data-ttu-id="9d1b0-144">Например, если перед командой **говорите** [**проигрывать**](play-method.md) «**жестуреригхт**», то на сервере будет воспроизводиться **жестуреригхт** , а затем анимация **жестуреригхт** .</span><span class="sxs-lookup"><span data-stu-id="9d1b0-144">For example, if you preceded the **Speak** command with a [**Play**](play-method.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="9d1b0-145">Если последняя воспроизводимая анимация не имеет речи, агент воспроизводит анимацию, назначенную состоянию **речи** символа.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-145">If the last animation played has no speaking animation, Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="9d1b0-146">Если вы выберете **разговор** и канал звука занят, звуковые выходные данные не будут слышны, а текст отобразится в выноске.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-146">If you call **Speak** and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span>

<span data-ttu-id="9d1b0-147">Автоматическое разбиение слов агента в выноске обрывает слова, используя пробелы (например, пробел или знак табуляции).</span><span class="sxs-lookup"><span data-stu-id="9d1b0-147">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="9d1b0-148">Однако, если это невозможно, может нарушиться слово, чтобы уместить всплывающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-148">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="9d1b0-149">В таких языках, как японский, китайский и тайский, если пробелы не используются для разбиения слов, вставьте символ пробела нулевой ширины (0x200B) в Юникоде между символами, чтобы определить логические разрывы слов.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-149">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="9d1b0-150">Свойство [**включено**](enabled-property.md) для всплывающей подсказки также должно иметь **значение true** для отображаемого текста.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-150">The word balloon's [**Enabled**](enabled-property.md) property must also be **True** for text to display.</span></span>

 

> [!Note]  
> <span data-ttu-id="9d1b0-151">Задайте идентификатор языка символа (с помощью параметра **LanguageID** символа перед использованием метода **говорите** , чтобы обеспечить отображение текста внутри всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="9d1b0-151">Set the character's language ID (by setting the character's **LanguageID** before using the **Speak** method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="9d1b0-152">См. также:</span><span class="sxs-lookup"><span data-stu-id="9d1b0-152">See Also</span></span>

<span data-ttu-id="9d1b0-153">Событие [**закладки**](bookmark-event.md), [**событие рекуестстарт**](requeststart-event.md), [**событие рекуесткомплете**](requestcomplete-event.md)</span><span class="sxs-lookup"><span data-stu-id="9d1b0-153">[**Bookmark event**](bookmark-event.md), [**RequestStart event**](requeststart-event.md), [**RequestComplete event**](requestcomplete-event.md)</span></span>


 

 