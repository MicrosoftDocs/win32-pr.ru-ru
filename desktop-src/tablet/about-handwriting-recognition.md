---
description: Планшетный ПК содержит технологию распознавания рукописного ввода, которая чаще всего используется в виде рукописного текста.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: О распознавании рукописного текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713126"
---
# <a name="about-handwriting-recognition"></a><span data-ttu-id="b3748-103">О распознавании рукописного текста</span><span class="sxs-lookup"><span data-stu-id="b3748-103">About Handwriting Recognition</span></span>

<span data-ttu-id="b3748-104">Планшетный ПК содержит технологию распознавания рукописного ввода, которая чаще всего используется в виде рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="b3748-104">Tablet PC includes technology for recognizing ink input that is most commonly in the form of handwriting.</span></span> <span data-ttu-id="b3748-105">Программный модуль, обеспечивающий распознавание, называется распознавателем.</span><span class="sxs-lookup"><span data-stu-id="b3748-105">The software module that provides the recognition is called a recognizer.</span></span> <span data-ttu-id="b3748-106">Распознаватель распознает один язык, группу связанных языков или класс связанных объектов, таких как музыкальные заметки, системные жесты или геометрические фигуры.</span><span class="sxs-lookup"><span data-stu-id="b3748-106">A recognizer recognizes one language, a group of related languages, or a class of related objects such as musical notes, system gestures, or geometric shapes.</span></span> <span data-ttu-id="b3748-107">Можно динамически добавлять распознаватели в систему служб рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="b3748-107">You can dynamically add recognizers to the ink services system.</span></span>

## <a name="recognition-steps"></a><span data-ttu-id="b3748-108">Действия по распознаванию</span><span class="sxs-lookup"><span data-stu-id="b3748-108">Recognition Steps</span></span>

<span data-ttu-id="b3748-109">Распознавание обрабатывается с помощью контекста распознавателя.</span><span class="sxs-lookup"><span data-stu-id="b3748-109">Recognition is handled through the use of a recognizer context.</span></span> <span data-ttu-id="b3748-110">Распознавание состоит из четырех основных этапов:</span><span class="sxs-lookup"><span data-stu-id="b3748-110">Recognition consists of four basic steps:</span></span>

1.  <span data-ttu-id="b3748-111">Настройка ограничений распознавания:</span><span class="sxs-lookup"><span data-stu-id="b3748-111">Setting up the recognition constraints by:</span></span>
    -   <span data-ttu-id="b3748-112">Выбор распознавателя и режима ввода (геометрические ограничения).</span><span class="sxs-lookup"><span data-stu-id="b3748-112">Selecting the recognizer and input mode (geometric constraints).</span></span>
    -   <span data-ttu-id="b3748-113">Настройка ограничений языка.</span><span class="sxs-lookup"><span data-stu-id="b3748-113">Setting the language constraints.</span></span> <span data-ttu-id="b3748-114">Например, можно ограничить ввод буквенно-цифровыми символами или передать схемы для помощи распознавателя.</span><span class="sxs-lookup"><span data-stu-id="b3748-114">For example, you can restrict input to alphanumeric characters or you can pass schemas to assist the recognizer.</span></span>
2.  <span data-ttu-id="b3748-115">Отправка рукописного ввода в распознаватель.</span><span class="sxs-lookup"><span data-stu-id="b3748-115">Sending ink to the recognizer.</span></span>
3.  <span data-ttu-id="b3748-116">Обработка входных данных (распознавание).</span><span class="sxs-lookup"><span data-stu-id="b3748-116">Processing the input (recognizing).</span></span>
4.  <span data-ttu-id="b3748-117">Возврат результатов распознавания.</span><span class="sxs-lookup"><span data-stu-id="b3748-117">Returning the results of the recognition.</span></span>

<span data-ttu-id="b3748-118">Шаги 2 и 3 могут повторяться в цикле, или все рукописные штрихи могут быть добавлены к рукописному вводу до попыток распознавания.</span><span class="sxs-lookup"><span data-stu-id="b3748-118">Steps 2 and 3 may be repeated in a loop, or all of the ink strokes may be added to the ink before recognition is attempted.</span></span>

## <a name="samples-and-related-topics"></a><span data-ttu-id="b3748-119">Примеры и связанные разделы</span><span class="sxs-lookup"><span data-stu-id="b3748-119">Samples and Related Topics</span></span>

<span data-ttu-id="b3748-120">[Образец расширенного распознавания](advanced-recognition-sample.md) демонстрирует использование распознавателей с объектами [**рукописного ввода**](inkdisp-class.md) для распознавания рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="b3748-120">[Advanced Recognition Sample](advanced-recognition-sample.md) demonstrates how to use recognizers with [**Ink**](inkdisp-class.md) objects to perform ink recognition.</span></span>

<span data-ttu-id="b3748-121">[Пример шаблона библиотеки DLL распознавателя](recognizer-dll-sample-template.md) содержит шаблон для создания библиотеки DLL распознавателя.</span><span class="sxs-lookup"><span data-stu-id="b3748-121">[Recognizer DLL Sample Template](recognizer-dll-sample-template.md) contains a template for creating a recognizer DLL.</span></span> <span data-ttu-id="b3748-122">Шаблон содержит функции для регистрации и отмены регистрации сервера, а также скелеты основных функций распознавателя.</span><span class="sxs-lookup"><span data-stu-id="b3748-122">The template contains functions for registering and unregistering the server, as well as skeletons for primary recognizer functions.</span></span>

<span data-ttu-id="b3748-123">В следующих разделах описываются основные понятия, лежащие в основе технологии распознавания Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="b3748-123">The following sections describe the basic concepts behind the Tablet PC recognition technology.</span></span> <span data-ttu-id="b3748-124">Подробные сведения о создании пользовательских распознавателей см. [в разделе Создание распознавателя](creating-a-recognizer.md).</span><span class="sxs-lookup"><span data-stu-id="b3748-124">For detailed information about creating custom recognizers, see [Creating a Recognizer](creating-a-recognizer.md).</span></span>

-   [<span data-ttu-id="b3748-125">Распознаватели текста</span><span class="sxs-lookup"><span data-stu-id="b3748-125">Text Recognizers</span></span>](text-recognizers.md)
-   [<span data-ttu-id="b3748-126">Распознаватели объектов</span><span class="sxs-lookup"><span data-stu-id="b3748-126">Object Recognizers</span></span>](object-recognizers.md)
-   [<span data-ttu-id="b3748-127">Использование коллекции распознавателей</span><span class="sxs-lookup"><span data-stu-id="b3748-127">Using the Recognizers Collection</span></span>](using-the-recognizers-collection.md)
-   [<span data-ttu-id="b3748-128">Контекст распознавателя</span><span class="sxs-lookup"><span data-stu-id="b3748-128">Recognizer Context</span></span>](recognizer-context.md)
-   [<span data-ttu-id="b3748-129">Сегменты распознавания</span><span class="sxs-lookup"><span data-stu-id="b3748-129">Recognition Segments</span></span>](recognition-segments.md)
-   [<span data-ttu-id="b3748-130">Распознавание повернутого текста</span><span class="sxs-lookup"><span data-stu-id="b3748-130">Recognition of Angled Text</span></span>](recognition-of-angled-text.md)
-   [<span data-ttu-id="b3748-131">Поддержка переупорядочивания перьев распознавателя</span><span class="sxs-lookup"><span data-stu-id="b3748-131">Recognizer Stroke Reordering Support</span></span>](recognizer-stroke-reordering-support.md)
-   [<span data-ttu-id="b3748-132">Словари и Фактоидс</span><span class="sxs-lookup"><span data-stu-id="b3748-132">Dictionaries and Factoids</span></span>](dictionaries-and-factoids.md)
-   <span data-ttu-id="b3748-133">[Свойство достоверности \[ о распознавании\]](confidence-property--about-recognition.md)</span><span class="sxs-lookup"><span data-stu-id="b3748-133">[Confidence Property \[About Recognition\]](confidence-property--about-recognition.md)</span></span>
-   [<span data-ttu-id="b3748-134">Варианты</span><span class="sxs-lookup"><span data-stu-id="b3748-134">Alternates</span></span>](alternates.md)
-   [<span data-ttu-id="b3748-135">Сегменты и варианты рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="b3748-135">Ink Segments and Alternates</span></span>](ink-segments-and-alternates.md)

 

 



