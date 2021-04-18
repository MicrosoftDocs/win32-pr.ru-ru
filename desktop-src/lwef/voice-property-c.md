---
title: Свойство Voice (объект Command)
description: Свойство Voice
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a8f9003b5200882fc01ee37edb868a261c68c7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691749"
---
# <a name="voice-property-command-object"></a><span data-ttu-id="6914a-103">Свойство Voice (объект Command)</span><span class="sxs-lookup"><span data-stu-id="6914a-103">Voice Property (Command Object)</span></span>

<span data-ttu-id="6914a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6914a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6914a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="6914a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6914a-106">Возвращает или задает текст, который передается в грамматику обработчика речи (для распознавания) для сопоставления этой [**команды**](/windows/desktop/lwef/the-command-object) с символом.</span><span class="sxs-lookup"><span data-stu-id="6914a-106">Returns or sets the text that is passed to the speech engine grammar (for recognition) for matching this [**Command**](/windows/desktop/lwef/the-command-object) for the character.</span></span>

</dd> <dt>

<span data-ttu-id="6914a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="6914a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6914a-108">\*Агент \***. Символы ("**_чарактерид_*_"). Команды ("_*_имя_\*_")._ \*  \[  =  *Строка* голоса\]</span><span class="sxs-lookup"><span data-stu-id="6914a-108">*agent\***.Characters ("**_CharacterID_*_").Commands ("_*_name_*_").Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="6914a-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="6914a-109">Part</span></span>     | <span data-ttu-id="6914a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6914a-110">Description</span></span>                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6914a-111">*string*</span><span class="sxs-lookup"><span data-stu-id="6914a-111">*string*</span></span> | <span data-ttu-id="6914a-112">Строковое выражение, соответствующее словам или фразе, используемым модулем распознавания речи для распознавания этой [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="6914a-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6914a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6914a-113">Remarks</span></span>

<span data-ttu-id="6914a-114">Если этот параметр не указан, [**воицекаптион**](voicecaption-property.md) для объекта [**Commands**](/windows/desktop/lwef/the-commands-collection-object) не отображается в окне "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="6914a-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span> <span data-ttu-id="6914a-115">Если указать параметр [**голоса**](voice-property.md) , но не **Воицекаптион** (или [**заголовок**](https://www.bing.com/search?q=**Caption**)), команда не будет отображаться в окне "Voice Commands", но она будет доступна для передачи голоса, когда клиентское приложение станет входным.</span><span class="sxs-lookup"><span data-stu-id="6914a-115">If you specify a [**Voice**](voice-property.md) parameter but not a **VoiceCaption** (or [**Caption**](https://www.bing.com/search?q=**Caption**)), the command will not appear in the Voice Commands Window, but it will be voice-accessible when the client application becomes input-active.</span></span>

<span data-ttu-id="6914a-116">Строковое выражение может включать в себя квадратные скобки ( \[ \] ) для обозначения дополнительных слов и символов вертикальной черты ( \| ) для указания альтернативных строк.</span><span class="sxs-lookup"><span data-stu-id="6914a-116">Your string expression can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="6914a-117">Альтернативные варианты должны быть заключены в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="6914a-117">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="6914a-118">Например, "(Привет! \[ \] \| Привет!)" говорит обработчику распознавания речи, что для команды нужно принять "Hello," Hello "или" Hi ".</span><span class="sxs-lookup"><span data-stu-id="6914a-118">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="6914a-119">Не забывайте включать в скобки и скобки соответствующие пробелы, а также текст, заключенный в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="6914a-119">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="6914a-120">Оператор Star () можно использовать, \* чтобы указать ноль или несколько экземпляров слов, входящих в группу, или оператор «плюс» (+), чтобы указать один или несколько экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6914a-120">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="6914a-121">Например, следующий пример приводит к грамматике, которая поддерживает команду "попробовать это", "Попробуйте", "Попробуйте это", с неограниченными итерациями ".</span><span class="sxs-lookup"><span data-stu-id="6914a-121">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="6914a-122">Следующий формат грамматики исключает "попробовать это", так как оператор + определяет по крайней мере один экземпляр ".</span><span class="sxs-lookup"><span data-stu-id="6914a-122">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="6914a-123">Операторы повторения следуют обычным правилам приоритета и применяются к непосредственно предшествующему текстовому элементу.</span><span class="sxs-lookup"><span data-stu-id="6914a-123">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="6914a-124">Например, следующая грамматика приводит к последующим результатам: "Нью Йорк" и "Нью Йорк York", но не "Нью Москва".</span><span class="sxs-lookup"><span data-stu-id="6914a-124">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="6914a-125">Поэтому обычно следует использовать эти операторы с символами группирования.</span><span class="sxs-lookup"><span data-stu-id="6914a-125">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="6914a-126">Например, следующая грамматика включает в себя "Нью Йорк" и "Нью Йорк":</span><span class="sxs-lookup"><span data-stu-id="6914a-126">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="6914a-127">Операторы повторения полезны, если необходимо составить грамматику, включающую повторяющуюся последовательность, например номер телефона или спецификацию списка элементов.</span><span class="sxs-lookup"><span data-stu-id="6914a-127">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="6914a-128">Хотя операторы также можно использовать с необязательным символом группирования квадратных скобок, это может снизить эффективность обработки грамматики агентом.</span><span class="sxs-lookup"><span data-stu-id="6914a-128">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="6914a-129">Кроме того, можно использовать многоточие (...) для поддержки поиска *слов*, то есть сообщить модулю распознавания речи о необходимости пропускать слова, пропускаемые в этой должности, в фразе (иногда называемых словами- *мусором* ).</span><span class="sxs-lookup"><span data-stu-id="6914a-129">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="6914a-130">Таким образом, обработчик речи распознает только определенные слова в строке независимо от того, когда речь поступала с соседними словами или фразами.</span><span class="sxs-lookup"><span data-stu-id="6914a-130">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="6914a-131">Например, если для этого свойства задано значение " \[ ... \] проверить почту \[ ... \] "обработчик распознавания речи будет сопоставлять такие фразы, как" проверить почту "или" проверить почту ", с помощью этой команды.</span><span class="sxs-lookup"><span data-stu-id="6914a-131">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="6914a-132">Многоточие можно использовать в любом месте строки.</span><span class="sxs-lookup"><span data-stu-id="6914a-132">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="6914a-133">Однако будьте внимательны при использовании этой методики, так как это может привести к увеличению потенциальных нежелательных совпадений.</span><span class="sxs-lookup"><span data-stu-id="6914a-133">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="6914a-134">При определении грамматики слова для команды включите по крайней мере одно необходимое слово; то есть не указывайте только необязательные слова.</span><span class="sxs-lookup"><span data-stu-id="6914a-134">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="6914a-135">Кроме того, убедитесь, что слово содержит только произношенные слова и буквы.</span><span class="sxs-lookup"><span data-stu-id="6914a-135">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="6914a-136">Для чисел лучше использовать слово, а не однозначное представление.</span><span class="sxs-lookup"><span data-stu-id="6914a-136">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="6914a-137">Например, "345" не является хорошей формой грамматики.</span><span class="sxs-lookup"><span data-stu-id="6914a-137">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="6914a-138">Аналогичным образом вместо «IEEE» используется «I Triple E».</span><span class="sxs-lookup"><span data-stu-id="6914a-138">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="6914a-139">Кроме того, не указывайте знаки препинания и символы.</span><span class="sxs-lookup"><span data-stu-id="6914a-139">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="6914a-140">Например, вместо "The \# $1 Пицца!" используйте "число 1 10 доллара пиццы".</span><span class="sxs-lookup"><span data-stu-id="6914a-140">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="6914a-141">Включение нерегулярных символов или символов для одной команды может привести к тому, что обработчику речи не удастся скомпилировать грамматику для всех команд.</span><span class="sxs-lookup"><span data-stu-id="6914a-141">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="6914a-142">Наконец, сделайте свой параметр голоса как можно более отличающимся от других определяемых вами речевых команд.</span><span class="sxs-lookup"><span data-stu-id="6914a-142">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="6914a-143">Чем больше сходство между грамматикой голоса для команд, тем выше вероятность того, что обработчик речи выполнит ошибку распознавания.</span><span class="sxs-lookup"><span data-stu-id="6914a-143">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="6914a-144">Можно также использовать оценку достоверности, чтобы лучше отличать две команды, которые могут иметь схожую или подобную грамматику голоса.</span><span class="sxs-lookup"><span data-stu-id="6914a-144">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="6914a-145">Можно включить слова в грамматику в виде *текста « \\ произношение*», где *текст* — это отображаемый текст, а *произношение* — текст, поясняющий произношение.</span><span class="sxs-lookup"><span data-stu-id="6914a-145">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="6914a-146">Например, грамматика «первое \\ Начало» будет распознается, когда пользователь говорит «First», но [**командное**](/windows/desktop/lwef/the-command-object) событие возвратит текст «первое \\ имя».</span><span class="sxs-lookup"><span data-stu-id="6914a-146">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](/windows/desktop/lwef/the-command-object) event will return the text, "1st\\first".</span></span> <span data-ttu-id="6914a-147">Можно также использовать IPA (Международный фонетический алфавит), чтобы указать произношение, начинающееся с символа решетки (" \# "), а затем включить текст, представляющий произношение IPA.</span><span class="sxs-lookup"><span data-stu-id="6914a-147">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="6914a-148">Для модулей распознавания речи японского языка можно определить грамматику в виде *японской азбуки \\*, уменьшая альтернативные произношение и увеличивая точность.</span><span class="sxs-lookup"><span data-stu-id="6914a-148">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="6914a-149">(Порядок сортировки обратно для обеспечения обратной совместимости.) Это особенно важно для произношения правильных имен в канджи.</span><span class="sxs-lookup"><span data-stu-id="6914a-149">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="6914a-150">Однако можно просто передать кандзи без японской азбуки, в этом случае подсистема должна прослушивать все приемлемые произношения для кандзи.</span><span class="sxs-lookup"><span data-stu-id="6914a-150">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="6914a-151">Можно также передать только символ Кана.</span><span class="sxs-lookup"><span data-stu-id="6914a-151">You can also pass in just Kana.</span></span>

<span data-ttu-id="6914a-152">Также обратите внимание, что для языков, таких как японский, китайский и тайский, которые не используют пробелы для обозначения разрывов слов, вставьте символ пробела нулевой ширины в Юникоде (0x200B), чтобы указать логические разрывы слов.</span><span class="sxs-lookup"><span data-stu-id="6914a-152">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="6914a-153">За исключением ошибок, использующих символы форматирования при группировании или повторении, агент не будет сообщать об ошибках в грамматике, если только сам обработчик не сообщит об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6914a-153">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="6914a-154">Если вы передали текст в грамматике, которую модуль не смог скомпилировать, но обработчик не сможет обрабатывать и возвращать ошибку, агент не может сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6914a-154">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="6914a-155">Поэтому клиентское приложение должно тщательно определять грамматику для свойства [**Voice**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="6914a-155">Therefore, the client application must be carefully define grammar for the [**Voice**](voice-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="6914a-156">Доступные функции грамматики могут зависеть от модуля распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="6914a-156">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="6914a-157">Чтобы определить, какие параметры грамматики поддерживаются, вы можете узнать у поставщика подсистемы.</span><span class="sxs-lookup"><span data-stu-id="6914a-157">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="6914a-158">Используйте [**срмодеид**](srmodeid-property.md) для использования определенного механизма.</span><span class="sxs-lookup"><span data-stu-id="6914a-158">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="6914a-159">Операция с этим свойством зависит от состояния свойства распознавания речи сервера.</span><span class="sxs-lookup"><span data-stu-id="6914a-159">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="6914a-160">Например, если распознавание речи отключено или не установлено, это свойство не действует.</span><span class="sxs-lookup"><span data-stu-id="6914a-160">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
