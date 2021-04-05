---
title: Написание кода события
description: Написание кода события
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Обложки проигрывателя Windows Media, написание кода
- обложки, написание кода
- события, написание кода
- Написание кода для обложек, о
- Обложки проигрывателя Windows Media, события
- обложки, события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068581"
---
# <a name="writing-event-code"></a><span data-ttu-id="fbcf9-109">Написание кода события</span><span class="sxs-lookup"><span data-stu-id="fbcf9-109">Writing Event Code</span></span>

<span data-ttu-id="fbcf9-110">События обрабатываются аналогично атрибутам.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-110">Events are treated similarly to attributes.</span></span> <span data-ttu-id="fbcf9-111">Необходимо присвоить событию значение, а значение — это код, который будет выполняться при наступлении события.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-111">You must give the event a value, and the value is the code you want to run when the event happens.</span></span> <span data-ttu-id="fbcf9-112">Слово «ON» добавляется в начало имени события; Например, событие Click станет **OnClick**.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-112">The word "on" is added to the front of the event name; for example, the click event will become **onclick**.</span></span>

<span data-ttu-id="fbcf9-113">Значение события указывается в двойных кавычках и начинается с слова JScript, за которым следует двоеточие.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-113">The event value is in double quotes and starts with the word JScript followed by a colon.</span></span> <span data-ttu-id="fbcf9-114">Код, который вы хотите запустить, поступает после точки с запятой и закрывающими двойными кавычками.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-114">The code you want to run comes next, followed by a semicolon and the closing double quotes.</span></span> <span data-ttu-id="fbcf9-115">Например, чтобы закончить воспроизведение при нажатии пользователем кнопки, введите следующий код в качестве атрибута в коде элемента **кнопки** :</span><span class="sxs-lookup"><span data-stu-id="fbcf9-115">For example, to stop playing when the user clicks on a button, type the following as an attribute in your **BUTTON** element code:</span></span>


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



<span data-ttu-id="fbcf9-116">Если у вас есть код, требующий кавычек, используйте одинарные кавычки.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-116">If you have a code that requires quotes, use single quotes.</span></span> <span data-ttu-id="fbcf9-117">Будьте осторожны при использовании кавычек, чтобы они были правильно сбалансированы.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-117">Care must be taken when using quotation marks so that they are balanced properly.</span></span> <span data-ttu-id="fbcf9-118">Ниже приведен пример использования обоих типов:</span><span class="sxs-lookup"><span data-stu-id="fbcf9-118">Here is an example of using both types:</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



<span data-ttu-id="fbcf9-119">Можно также изменить атрибуты обложки при обработке внешнего события.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-119">You can also change attributes of your skin when handling an external event.</span></span> <span data-ttu-id="fbcf9-120">Например, чтобы закрыть представление с именем myView, можно ввести следующее:</span><span class="sxs-lookup"><span data-stu-id="fbcf9-120">For example, to close a view named myView, you could type:</span></span>


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a><span data-ttu-id="fbcf9-121">См. также</span><span class="sxs-lookup"><span data-stu-id="fbcf9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbcf9-122">**Обработка событий**</span><span class="sxs-lookup"><span data-stu-id="fbcf9-122">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




