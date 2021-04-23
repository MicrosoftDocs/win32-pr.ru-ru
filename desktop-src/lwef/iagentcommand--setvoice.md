---
title: Иаженткомманд Сетвоице
description: Иаженткомманд Сетвоице
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bed7e86cb93824fc26c770c1d01336077fda39
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700859"
---
# <a name="iagentcommandsetvoice"></a><span data-ttu-id="af3c3-103">Иаженткомманд:: Сетвоице</span><span class="sxs-lookup"><span data-stu-id="af3c3-103">IAgentCommand::SetVoice</span></span>

<span data-ttu-id="af3c3-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af3c3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

<span data-ttu-id="af3c3-105">Задает свойство [**Voice**](voice-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="af3c3-105">Sets the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="af3c3-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="af3c3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="af3c3-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*бсзвоице*</span><span class="sxs-lookup"><span data-stu-id="af3c3-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="af3c3-108">Значение типа BSTR, указывающее текст для свойства [**Voice**](voice-property.md) [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="af3c3-108">A BSTR that specifies the text for the [**Voice**](voice-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="af3c3-109">Для [**команды**](/windows/desktop/lwef/the-command-object) должно быть задано свойство [**Voice**](voice-property.md) , а для свойства [**Enabled**](enabled-property.md) — значение доступ к голосовым данным.</span><span class="sxs-lookup"><span data-stu-id="af3c3-109">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Voice**](voice-property.md) property and [**Enabled**](enabled-property.md) property set to be voice-accessible.</span></span> <span data-ttu-id="af3c3-110">Кроме того, свойство [**воицекаптион**](voicecaption-property.md) должно иметь значение, отображаемое в **окне "Voice Commands**".</span><span class="sxs-lookup"><span data-stu-id="af3c3-110">It also must have its [**VoiceCaption**](voicecaption-property.md) property set to appear in the **Voice Commands Window**.</span></span> <span data-ttu-id="af3c3-111">(Для обеспечения обратной совместимости при отсутствии **воицекаптион** используется параметр [**Caption**](caption-property.md) .)</span><span class="sxs-lookup"><span data-stu-id="af3c3-111">(For backward compatibility, if there is no **VoiceCaption**, the [**Caption**](caption-property.md) setting is used.)</span></span>

<span data-ttu-id="af3c3-112">Указываемое выражение BSTR может включать в себя квадратные скобки ( \[ \] ) для обозначения дополнительных слов и символов вертикальной черты ( \| ) для указания альтернативных строк.</span><span class="sxs-lookup"><span data-stu-id="af3c3-112">The BSTR expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="af3c3-113">Альтернативные варианты должны быть заключены в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="af3c3-113">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="af3c3-114">Например, "(Привет! \[ \] \| Привет!)" говорит обработчику распознавания речи, что для команды нужно принять "Hello," Hello "или" Hi ".</span><span class="sxs-lookup"><span data-stu-id="af3c3-114">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="af3c3-115">Не забывайте включать в скобки и скобки соответствующие пробелы, а также текст, заключенный в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="af3c3-115">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="af3c3-116">Оператор Star () можно использовать, \* чтобы указать ноль или несколько экземпляров слов, входящих в группу, или оператор «плюс» (+), чтобы указать один или несколько экземпляров.</span><span class="sxs-lookup"><span data-stu-id="af3c3-116">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="af3c3-117">Например, следующий пример приводит к грамматике, которая поддерживает команду "попробовать это", "Попробуйте" и "Попробуйте", с неограниченными итерациями ".</span><span class="sxs-lookup"><span data-stu-id="af3c3-117">For example, the following results in a grammar that supports "try this", "please try this", and "please please try this", with unlimited iterations of "please":</span></span>

``` syntax
   "please* try this"
```

<span data-ttu-id="af3c3-118">Следующий формат грамматики исключает "попробовать это", так как оператор + определяет по крайней мере один экземпляр ".</span><span class="sxs-lookup"><span data-stu-id="af3c3-118">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>

``` syntax
   "please+ try this"
```

<span data-ttu-id="af3c3-119">Операторы повторения следуют обычным правилам приоритета и применяются к непосредственно предшествующему текстовому элементу.</span><span class="sxs-lookup"><span data-stu-id="af3c3-119">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="af3c3-120">Например, следующая грамматика приводит к последующим результатам: "Нью Йорк" и "Нью Йорк York", но не "Нью Москва".</span><span class="sxs-lookup"><span data-stu-id="af3c3-120">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>

``` syntax
   "New York+"
```

<span data-ttu-id="af3c3-121">Поэтому, как правило, необходимо использовать эти операторы с символами группирования.</span><span class="sxs-lookup"><span data-stu-id="af3c3-121">Therefore, you will typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="af3c3-122">Например, следующая грамматика включает в себя "Нью Йорк" и "Нью Йорк":</span><span class="sxs-lookup"><span data-stu-id="af3c3-122">For example, the following grammar includes both "New York" and "New York New York":</span></span>

``` syntax
   "(New York)+"
```

<span data-ttu-id="af3c3-123">Операторы повторения полезны, если необходимо составить грамматику, которая включает повторяющиеся последовательности, такие как номер телефона или спецификация списка элементов:</span><span class="sxs-lookup"><span data-stu-id="af3c3-123">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items:</span></span>

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

<span data-ttu-id="af3c3-124">Хотя операторы также можно использовать с квадратными скобками (необязательный символ группирования), это может снизить эффективность обработки грамматики агента.</span><span class="sxs-lookup"><span data-stu-id="af3c3-124">Although the operators can also be used with the square brackets (an optional grouping character), doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="af3c3-125">Кроме того, можно использовать многоточие (...) для поддержки поиска *слов*, то есть сообщить модулю распознавания речи о необходимости пропускать слова, пропускаемые в этой должности, в фразе (иногда называемых словами- *мусором* ).</span><span class="sxs-lookup"><span data-stu-id="af3c3-125">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="af3c3-126">Таким образом, обработчик речи распознает только определенные слова в строке независимо от того, когда речь поступала с соседними словами или фразами.</span><span class="sxs-lookup"><span data-stu-id="af3c3-126">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="af3c3-127">Например, если для этого свойства задано значение " \[ ... \] проверить почту \[ ... \] "модуль распознавания речи будет сопоставлять такие фразы, как" проверить почту "или" проверить почту ", с помощью этой команды.</span><span class="sxs-lookup"><span data-stu-id="af3c3-127">For example, if you set this property to "\[...\] check mail \[...\]" the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="af3c3-128">Многоточие можно использовать в любом месте строки.</span><span class="sxs-lookup"><span data-stu-id="af3c3-128">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="af3c3-129">Однако будьте внимательны при использовании этого метода, так как параметры голоса с многоточием могут увеличить потенциал нежелательных совпадений.</span><span class="sxs-lookup"><span data-stu-id="af3c3-129">However, be careful using this technique, because voice settings with ellipses may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="af3c3-130">При определении слов и грамматики для команды всегда обязательно включите по крайней мере одно необходимое слово. то есть не указывайте только необязательные слова.</span><span class="sxs-lookup"><span data-stu-id="af3c3-130">When defining the words and grammar for your command, always make sure that you include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="af3c3-131">Кроме того, убедитесь, что слово содержит только произношенные слова и буквы.</span><span class="sxs-lookup"><span data-stu-id="af3c3-131">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="af3c3-132">Для чисел лучше использовать слова вместо числового представления.</span><span class="sxs-lookup"><span data-stu-id="af3c3-132">For numbers, it is better to spell out the word rather than using the numeric representation.</span></span> <span data-ttu-id="af3c3-133">Кроме того, не указывайте знаки препинания и символы.</span><span class="sxs-lookup"><span data-stu-id="af3c3-133">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="af3c3-134">Например, вместо "The \# $1 Пицца!" используйте "число 1 10 доллара пиццы".</span><span class="sxs-lookup"><span data-stu-id="af3c3-134">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="af3c3-135">Включение нерегулярных символов или символов для одной команды может привести к тому, что обработчику речи не удастся скомпилировать грамматику для всех команд.</span><span class="sxs-lookup"><span data-stu-id="af3c3-135">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="af3c3-136">Наконец, сделайте свой параметр голоса как можно более отличающимся от других определяемых вами речевых команд.</span><span class="sxs-lookup"><span data-stu-id="af3c3-136">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="af3c3-137">Чем больше сходство между грамматикой голоса для команд, тем выше вероятность того, что обработчик речи выполнит ошибку распознавания.</span><span class="sxs-lookup"><span data-stu-id="af3c3-137">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="af3c3-138">Можно также использовать оценку достоверности, чтобы лучше отличать две команды, которые могут иметь схожую или подобную грамматику голоса.</span><span class="sxs-lookup"><span data-stu-id="af3c3-138">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="af3c3-139">Установка свойства [**Voice**](voice-property.md) для [**команды**](/windows/desktop/lwef/the-command-object) автоматически включает речевые службы агента, делая доступными ключ прослушивания и TIP прослушивания.</span><span class="sxs-lookup"><span data-stu-id="af3c3-139">Setting the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) automatically enables Agent's speech services, making the Listening key and Listening Tip available.</span></span> <span data-ttu-id="af3c3-140">Однако он не загружает модуль распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="af3c3-140">However, it does not load the speech recognition engine.</span></span>

> [!Note]  
> <span data-ttu-id="af3c3-141">Доступные функции грамматики могут зависеть от модуля распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="af3c3-141">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="af3c3-142">Чтобы определить, какие параметры грамматики поддерживаются, вы можете узнать у поставщика подсистемы.</span><span class="sxs-lookup"><span data-stu-id="af3c3-142">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="af3c3-143">Чтобы указать подсистему, используйте [**иажентчарактерекс:: срмодеид**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) .</span><span class="sxs-lookup"><span data-stu-id="af3c3-143">Use [**IAgentCharacterEx::SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) to specify an engine.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="af3c3-144">См. также:</span><span class="sxs-lookup"><span data-stu-id="af3c3-144">See Also</span></span>

<span data-ttu-id="af3c3-145">[**Иаженткомманд:: Voice**](iagentcommand--getvoice.md), [**Иаженткомманд:: сеткаптион**](iagentcommand--setcaption.md), [**иаженткомманд:: Сетенаблед**](iagentcommand--setenabled.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: INSERT**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="af3c3-145">[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 