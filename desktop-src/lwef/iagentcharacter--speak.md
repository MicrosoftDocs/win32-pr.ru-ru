---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e290ab9037ee6f261445d4dfd00a206213cd26
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533155"
---
# <a name="iagentcharacterspeak"></a><span data-ttu-id="d18ac-103">Иажентчарактер:: говорите</span><span class="sxs-lookup"><span data-stu-id="d18ac-103">IAgentCharacter::Speak</span></span>

<span data-ttu-id="d18ac-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d18ac-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="d18ac-105">Говорит текст или звуковой файл.</span><span class="sxs-lookup"><span data-stu-id="d18ac-105">Speaks the text or sound file.</span></span>

-   <span data-ttu-id="d18ac-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d18ac-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d18ac-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*бсзтекст*</span><span class="sxs-lookup"><span data-stu-id="d18ac-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="d18ac-108">Текст, который должен говориться с символом.</span><span class="sxs-lookup"><span data-stu-id="d18ac-108">The text the character is to speak.</span></span>

</dd> <dt>

<span data-ttu-id="d18ac-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*бсзурл*</span><span class="sxs-lookup"><span data-stu-id="d18ac-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span></span>
</dt> <dd>

<span data-ttu-id="d18ac-110">URL-адрес (или спецификация файла) звукового файла, используемого для речевого вывода.</span><span class="sxs-lookup"><span data-stu-id="d18ac-110">The URL (or file specification) of a sound file to use for spoken output.</span></span> <span data-ttu-id="d18ac-111">Это может быть стандартный звуковой файл (. WAV) или лингвистическо Улучшенный звуковой файл (. ЛВВ).</span><span class="sxs-lookup"><span data-stu-id="d18ac-111">This can be a standard sound file (.WAV) or linguistically enhanced sound file (.LWV).</span></span>

</dd> <dt>

<span data-ttu-id="d18ac-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="d18ac-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="d18ac-113">Адрес переменной, которая получает идентификатор запроса [**говорите**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="d18ac-113">Address of a variable that receives the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="d18ac-114">Для использования этого метода с символом, настроенным для диктовки с помощью механизма преобразования текста в речь (TTS); просто укажите параметр *бсзтекст* .</span><span class="sxs-lookup"><span data-stu-id="d18ac-114">To use this method with a character configured to speak using a text-to-speech (TTS) engine; simply provide the *bszText* parameter.</span></span> <span data-ttu-id="d18ac-115">В параметре Бсзтекст можно включить символы вертикальной черты ( \| ), чтобы назначить альтернативные строки, чтобы каждый раз, когда сервер обрабатывает метод, случайно выбрать другую строку. </span><span class="sxs-lookup"><span data-stu-id="d18ac-115">You can include vertical bar characters (\|) in the *bszText* parameter to designate alternative strings, so that each time the server processes the method, it randomly choose a different string.</span></span> <span data-ttu-id="d18ac-116">Поддержка вывода TTS определяется при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d18ac-116">Support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="d18ac-117">Если для символа нужно использовать выходные данные звукового файла, укажите расположение файла в параметре *бсзурл* .</span><span class="sxs-lookup"><span data-stu-id="d18ac-117">If you want to use sound file output for the character, specify the location for the file in the *bszURL* parameter.</span></span> <span data-ttu-id="d18ac-118">При использовании протокола HTTP для загрузки звукового файла используйте метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) , чтобы обеспечить доступность файла перед использованием этого метода.</span><span class="sxs-lookup"><span data-stu-id="d18ac-118">When using the HTTP protocol to download a sound file, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the file before using this method.</span></span> <span data-ttu-id="d18ac-119">Можно использовать параметр *бсзтекст* для указания слов, отображаемых в тексте всплывающего слова символа.</span><span class="sxs-lookup"><span data-stu-id="d18ac-119">You can use the *bszText* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="d18ac-120">При указании лингвистическо расширенного звукового файла (. ЛВВ) для параметра *бсзурл* и не указывайте текст, параметр *бсзтекст* использует текст, хранящийся в файле.</span><span class="sxs-lookup"><span data-stu-id="d18ac-120">If you specify a linguistically enhanced sound file (.LWV) for the *bszURL* parameter and do not specify text, the *bszText* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="d18ac-121">Метод [**говорите**](/windows/desktop/lwef/iagentcharacter--speak) использует последнюю воспроизводимую анимацию, чтобы определить, какую анимацию речи следует воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="d18ac-121">The [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method uses the last animation played to determine which speaking animation to play.</span></span> <span data-ttu-id="d18ac-122">Например, если вы предшествует команду **говорите** с параметром [**иажентчарактер::P**](iagentcharacter--play.md) «**жестуреригхт**», то на сервере будет воспроизводиться **жестуреригхт** , а затем анимация **жестуреригхт** .</span><span class="sxs-lookup"><span data-stu-id="d18ac-122">For example, if you precede the **Speak** command with an [**IAgentCharacter::Play**](iagentcharacter--play.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="d18ac-123">Если последняя воспроизводимая анимация не имеет анимированной анимации, то Microsoft Agent воспроизводит анимацию, назначенную этому состоянию **речи** .</span><span class="sxs-lookup"><span data-stu-id="d18ac-123">If the last animation played has no speaking animation, then Microsoft Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="d18ac-124">Если вы выберете [**разговор**](/windows/desktop/lwef/iagentcharacter--speak) и канал звука занят, звуковые выходные данные не будут слышны, а текст отобразится в выноске.</span><span class="sxs-lookup"><span data-stu-id="d18ac-124">If you call [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span> <span data-ttu-id="d18ac-125">Для отображаемого текста свойство [Enabled](enabled-property.md) всплывающей программы должно иметь **значение true** .</span><span class="sxs-lookup"><span data-stu-id="d18ac-125">The word balloon's [Enabled](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="d18ac-126">Автоматическое разбиение слов Microsoft Agent в подсказке, разбивает слова, используя пробелы (например, пробел и знак табуляции).</span><span class="sxs-lookup"><span data-stu-id="d18ac-126">Microsoft Agent's automatic word breaking in the word balloon, breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="d18ac-127">Однако он может нарушить работу слова, чтобы вместить всплывающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="d18ac-127">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="d18ac-128">В таких языках, как японский, китайский и тайский, если пробелы не используются для разбиения слов на слова, вставьте символ нулевой ширины (0x200B) в Юникоде между символами, чтобы определить логические разрывы слов.</span><span class="sxs-lookup"><span data-stu-id="d18ac-128">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="d18ac-129">Задайте идентификатор языка символа (с помощью [**иажентчарактерекс:: сетлангуажеид**](iagentcharacterex--setlanguageid.md) перед использованием метода [**говорите**](/windows/desktop/lwef/iagentcharacter--speak) , чтобы обеспечить отображение текста внутри всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="d18ac-129">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d18ac-130">См. также:</span><span class="sxs-lookup"><span data-stu-id="d18ac-130">See Also</span></span>

<span data-ttu-id="d18ac-131">[**Иажентчарактер::Pный макет**](iagentcharacter--play.md), [**Иажентбаллун:: enable**](iagentballoon--getenabled.md), [**иажентчарактер::P готовка**](iagentcharacter--prepare.md)</span><span class="sxs-lookup"><span data-stu-id="d18ac-131">[**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md)</span></span>


 

 