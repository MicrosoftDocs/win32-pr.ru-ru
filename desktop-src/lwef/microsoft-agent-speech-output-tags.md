---
title: Теги речевого вывода агента Microsoft Agent
description: Теги речевого вывода агента Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888448"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="4505e-103">Теги речевого вывода агента Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="4505e-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="4505e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4505e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4505e-105">Службы Microsoft Agent поддерживают изменение речевого вывода с помощью специальных тегов, вставленных в текстовую строку речи.</span><span class="sxs-lookup"><span data-stu-id="4505e-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="4505e-106">Эти теги помогают изменить характеристики выходного выражения символа.</span><span class="sxs-lookup"><span data-stu-id="4505e-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="4505e-107">Теги вывода речи используют следующие правила синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="4505e-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="4505e-108">Все теги начинаются и заканчиваются символом обратной косой черты ( \) .</span><span class="sxs-lookup"><span data-stu-id="4505e-108">All tags begin and end with a backslash character (\).</span></span>
-   <span data-ttu-id="4505e-109">Один символ обратной косой черты не включен в теге.</span><span class="sxs-lookup"><span data-stu-id="4505e-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="4505e-110">Чтобы включить символ обратной косой черты в текстовый параметр тега, используйте двойную обратную косую черту ( \\ \) .</span><span class="sxs-lookup"><span data-stu-id="4505e-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\).</span></span>
-   <span data-ttu-id="4505e-111">В тегах не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="4505e-111">Tags are case-insensitive.</span></span> <span data-ttu-id="4505e-112">Например, \\ значение «смола» совпадает с \\ « \\ смолой» \\ .</span><span class="sxs-lookup"><span data-stu-id="4505e-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="4505e-113">Теги зависят от пробелов.</span><span class="sxs-lookup"><span data-stu-id="4505e-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="4505e-114">Например, \\ RST \\ не совпадает с \\ RST \\ .</span><span class="sxs-lookup"><span data-stu-id="4505e-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="4505e-115">Если не указано иное или не изменено другим тегом, речевое вывод оставляет набор характеристик, заданный тегом внутри текста, указанного в одном методе [**говорите**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="4505e-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="4505e-116">После завершения метода **произношения** речевые данные автоматически сбрасываются через определяемые пользователем параметры.</span><span class="sxs-lookup"><span data-stu-id="4505e-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="4505e-117">Некоторые теги содержат строки в кавычках.</span><span class="sxs-lookup"><span data-stu-id="4505e-117">Some tags include quoted strings.</span></span> <span data-ttu-id="4505e-118">Для некоторых языков программирования, таких как Visual Basic Scripting Edition (VBScript) и Visual Basic, это означает, что может потребоваться использование двух кавычек для обозначения параметра тега или сцепления символа двойной кавычки в составе строки.</span><span class="sxs-lookup"><span data-stu-id="4505e-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="4505e-119">Последнее показано в этом Visual Basic примере:</span><span class="sxs-lookup"><span data-stu-id="4505e-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="4505e-120">В языках C, C++ и Java™ программировании перед символами обратной косой черты и двойными кавычками.</span><span class="sxs-lookup"><span data-stu-id="4505e-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="4505e-121">Пример:</span><span class="sxs-lookup"><span data-stu-id="4505e-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="4505e-122">Для иностранных языков, поддерживающих символы в двухбайтовой кодировке (DBCS), для указания строковых параметров можно использовать двухбайтовые символы.</span><span class="sxs-lookup"><span data-stu-id="4505e-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="4505e-123">Однако Используйте однобайтовые символы для всех других параметров и символов, которые используются для определения тега, включая сам тег.</span><span class="sxs-lookup"><span data-stu-id="4505e-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="4505e-124">Поддерживаются следующие теги:</span><span class="sxs-lookup"><span data-stu-id="4505e-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="4505e-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="4505e-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="4505e-126">**CTX**</span><span class="sxs-lookup"><span data-stu-id="4505e-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="4505e-127">**Точек**</span><span class="sxs-lookup"><span data-stu-id="4505e-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="4505e-128">**LST**</span><span class="sxs-lookup"><span data-stu-id="4505e-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="4505e-129">**Таблица**</span><span class="sxs-lookup"><span data-stu-id="4505e-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="4505e-130">**мрк**</span><span class="sxs-lookup"><span data-stu-id="4505e-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="4505e-131">**пау**</span><span class="sxs-lookup"><span data-stu-id="4505e-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="4505e-132">**Медлен**</span><span class="sxs-lookup"><span data-stu-id="4505e-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="4505e-133">**RST**</span><span class="sxs-lookup"><span data-stu-id="4505e-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="4505e-134">**Политики**</span><span class="sxs-lookup"><span data-stu-id="4505e-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="4505e-135">**Т**</span><span class="sxs-lookup"><span data-stu-id="4505e-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="4505e-136">Теги в основном предназначены для настройки выходных данных преобразования текста в речь (TTS).</span><span class="sxs-lookup"><span data-stu-id="4505e-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="4505e-137">Только теги [**МРК**](mrk-tag.md) и [**Map**](map-tag.md) можно использовать с речевым выходом на основе файлов.</span><span class="sxs-lookup"><span data-stu-id="4505e-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="4505e-138">Microsoft Agent не поддерживает все теги, описанные в пакете Microsoft Speech SDK.</span><span class="sxs-lookup"><span data-stu-id="4505e-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="4505e-139">Параметры также могут различаться в зависимости от выбранного модуля TTS.</span><span class="sxs-lookup"><span data-stu-id="4505e-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="4505e-140">Вы можете задать конкретный модуль TTS с помощью [**ттсмодеид**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="4505e-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




