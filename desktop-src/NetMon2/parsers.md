---
description: Средство синтаксического анализа является компонентом сетевой монитор, который проверяет данные в отложенной записи и передает сведения о конкретном протоколе приложению, которое вызывает средство синтаксического анализа. Средство синтаксического анализа является пассивным, поскольку оно работает только при сетевой монитор или в эксперте.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896758"
---
# <a name="parser"></a><span data-ttu-id="5e799-104">Parser</span><span class="sxs-lookup"><span data-stu-id="5e799-104">Parser</span></span>

<span data-ttu-id="5e799-105">Средство синтаксического анализа является компонентом сетевой монитор, который проверяет данные в [*отложенной записи*](d.md)и передает сведения о конкретном протоколе приложению, которое вызывает средство синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="5e799-105">A parser is the Network Monitor component that inspects data in a [*delayed capture*](d.md), and passes specific protocol information to the application that calls the parser.</span></span> <span data-ttu-id="5e799-106">Средство синтаксического анализа является пассивным, поскольку оно работает только при сетевой монитор или в [*эксперте*](e.md) .</span><span class="sxs-lookup"><span data-stu-id="5e799-106">A parser is passive because it works only when Network Monitor or an [*expert*](e.md) call it.</span></span>

<span data-ttu-id="5e799-107">Каждый синтаксический анализатор определяет один протокол, и обычно средство синтаксического анализа реализуется в собственной библиотеке DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="5e799-107">Each parser identifies one protocol, and typically, a parser is implemented within its own parser DLL.</span></span> <span data-ttu-id="5e799-108">Однако библиотека DLL средства синтаксического анализа может содержать несколько средств синтаксического анализа, что означает, что одну библиотеку DLL можно использовать для обнаружения нескольких протоколов.</span><span class="sxs-lookup"><span data-stu-id="5e799-108">However, a parser DLL can contain multiple parsers which means that one DLL can be used to detect more than one protocol.</span></span>

<span data-ttu-id="5e799-109">Данные, передаваемые в средство синтаксического анализа, берутся из [*отложенной записи*](d.md)и передаются в средство синтаксического анализа по покадровой.</span><span class="sxs-lookup"><span data-stu-id="5e799-109">The data passed to a parser is taken from a [*delayed capture*](d.md), and passed to the parser on a frame-by-frame basis.</span></span> <span data-ttu-id="5e799-110">Невозможно проанализировать запись в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="5e799-110">You cannot parse a real-time capture.</span></span>

<span data-ttu-id="5e799-111">Для анализа данных в кадре средство синтаксического анализа должно распознать экземпляр протокола, определить свойства, существующие в экземпляре протокола, и присоединить определение свойства к каждому свойству.</span><span class="sxs-lookup"><span data-stu-id="5e799-111">To parse the data in a frame, the parser must recognize the protocol instance, identify the properties that exist in the protocol instance, and attach a property definition to each property.</span></span> <span data-ttu-id="5e799-112">Имейте в виду, что кадр содержит только поток данных.</span><span class="sxs-lookup"><span data-stu-id="5e799-112">Be aware that the frame contains only a stream of data.</span></span> <span data-ttu-id="5e799-113">Кадр не содержит данных, указывающих, какие протоколы или свойства протокола представляют данные.</span><span class="sxs-lookup"><span data-stu-id="5e799-113">The frame does not contain data that indicates which protocols or protocol properties the data represents.</span></span>

<span data-ttu-id="5e799-114">На следующем рисунке показан кадр, содержащий экземпляр протокола.</span><span class="sxs-lookup"><span data-stu-id="5e799-114">The following illustration shows a frame that contains an instance of a protocol.</span></span>

![кадр, содержащий экземпляр протокола](images/parser1.png)

<span data-ttu-id="5e799-116">Если сетевой монитор будет отображать проанализированные данные в пользовательском интерфейсе, средство синтаксического анализа должно отформатировать данные.</span><span class="sxs-lookup"><span data-stu-id="5e799-116">If Network Monitor is going to display parsed data in the UI, the parser must format the data.</span></span> <span data-ttu-id="5e799-117">Однако некоторые эксперты используют выходные данные средства синтаксического анализа программным образом и не отображают выходные данные в пользовательском интерфейсе сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="5e799-117">However, some experts use the parser output programmatically, and do not display the output in the Network Monitor UI.</span></span> <span data-ttu-id="5e799-118">Отображаемые данные включают как данные, определяемые синтаксическим анализатором, так и данные, содержащиеся в записи.</span><span class="sxs-lookup"><span data-stu-id="5e799-118">Displayed data includes both parser-defined data, and the data in the capture.</span></span> <span data-ttu-id="5e799-119">Например, средство синтаксического анализа обычно содержит как имя отображаемого свойства, так и данные в записи, связанной со свойством.</span><span class="sxs-lookup"><span data-stu-id="5e799-119">For example, the parser typically provides both a name for a property that is displayed, and the data in the capture that is associated with the property.</span></span>



| <span data-ttu-id="5e799-120">Сведения о</span><span class="sxs-lookup"><span data-stu-id="5e799-120">For information about</span></span>                                         | <span data-ttu-id="5e799-121">См.</span><span class="sxs-lookup"><span data-stu-id="5e799-121">See</span></span>                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="5e799-122">Какие точки входа должны быть реализованы в библиотеке DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="5e799-122">Which entry points must be implemented within the parser DLL.</span></span> | [<span data-ttu-id="5e799-123">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="5e799-123">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                 |
| <span data-ttu-id="5e799-124">Реализация функций экспорта библиотеки DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="5e799-124">How to implement parser DLL export functions.</span></span>                 | [<span data-ttu-id="5e799-125">Написание средства синтаксического анализа протокола</span><span class="sxs-lookup"><span data-stu-id="5e799-125">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="5e799-126">Какие функции и анализаторы структур используют.</span><span class="sxs-lookup"><span data-stu-id="5e799-126">Which functions and structures parsers use.</span></span>                   | [<span data-ttu-id="5e799-127">Функции и структуры средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="5e799-127">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



