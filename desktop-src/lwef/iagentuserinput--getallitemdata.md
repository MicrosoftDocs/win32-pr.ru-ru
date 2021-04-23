---
title: Иажентусеринпут Жеталлитемдата
description: Иажентусеринпут Жеталлитемдата
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486533"
---
# <a name="iagentuserinputgetallitemdata"></a><span data-ttu-id="14215-103">Иажентусеринпут:: Жеталлитемдата</span><span class="sxs-lookup"><span data-stu-id="14215-103">IAgentUserInput::GetAllItemData</span></span>

<span data-ttu-id="14215-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="14215-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

<span data-ttu-id="14215-105">Извлекает данные для всех вариантов [**команд**](command-event.md) , передаваемых в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="14215-105">Retrieves the data for all [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="14215-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="14215-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="14215-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*пдвитеминдицес*</span><span class="sxs-lookup"><span data-stu-id="14215-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span></span>
</dt> <dd>

<span data-ttu-id="14215-108">Адрес переменной, которая получает идентификаторы [**команд**](command-event.md) , переданных в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="14215-108">Address of a variable that receives the IDs of [**Commands**](command-event.md) passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="14215-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*плконфиденцес*</span><span class="sxs-lookup"><span data-stu-id="14215-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span></span>
</dt> <dd>

<span data-ttu-id="14215-110">Адрес переменной, получающей показатели достоверности для вариантов [**команд**](command-event.md) , передаваемых в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="14215-110">Address of a variable that receives the confidence scores for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="14215-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*пбсзтекст*</span><span class="sxs-lookup"><span data-stu-id="14215-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="14215-112">Адрес переменной, которая получает текст голоса для вариантов [**команд**](command-event.md) , передаваемых обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="14215-112">Address of a variable that receives the voice text for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="14215-113">Если речевое вход активирует [**иажентнотифисинк:: Command**](iagentnotifysink--command.md), сервер возвращает лучшее соответствие, второе — лучшее и третье соответствие, если они предоставляются модулем распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="14215-113">If speech input triggers [**IAgentNotifySink::Command**](iagentnotifysink--command.md), the server returns the best match, the second-best match, and the third-best match, if these are provided by the speech engine.</span></span> <span data-ttu-id="14215-114">Он обеспечивает относительный показатель достоверности в диапазоне от-100 до 100, а фактический текст "слышал" подсистемой распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="14215-114">It provides the relative confidence scores, in the range of -100 to 100, and actual text "heard" by the speech engine.</span></span> <span data-ttu-id="14215-115">Если наиболее подходящее совпадение было команда, предоставляемая сервером, сервер отправляет идентификатор NULL, но по-прежнему отправляет оценку достоверности и текст [**голоса**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="14215-115">If the best match was a server-supplied command, the server sends a NULL ID, but still sends a confidence score and the [**Voice**](voice-property.md) text.</span></span>

<span data-ttu-id="14215-116">Значение, если речевой ввод не является источником события; Например, если пользователь выбрал команду из всплывающего меню символа, сервер Microsoft Agent возвращает идентификатор выбранной [**команды**](command-event.md) с показателем достоверности 100 и голосовым текстом, равным null.</span><span class="sxs-lookup"><span data-stu-id="14215-116">If speech input was not the source for the event; for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the ID of the [**Command**](command-event.md) selected, with a confidence score of 100 and voice text as NULL.</span></span> <span data-ttu-id="14215-117">Другие варианты возвращают значение NULL с показателями достоверности ноль (0) и Voice Text как NULL.</span><span class="sxs-lookup"><span data-stu-id="14215-117">The other alternatives return as NULL with confidence scores of zero (0) and voice text as NULL.</span></span>

> [!Note]  
> <span data-ttu-id="14215-118">Не все модули распознавания речи могут возвращать все значения для всех параметров этого события.</span><span class="sxs-lookup"><span data-stu-id="14215-118">Not all speech recognition engines may return all the values for all the parameters of this event.</span></span> <span data-ttu-id="14215-119">Обратитесь к поставщику подсистемы, чтобы определить, поддерживает ли подсистема интерфейс API распознавания речи Майкрософт для возврата альтернатив и оценки достоверности.</span><span class="sxs-lookup"><span data-stu-id="14215-119">Check with your engine vendor to determine whether the engine supports the Microsoft Speech API interface for returning alternatives and confidence scores.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="14215-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="14215-120">See Also</span></span>

<span data-ttu-id="14215-121">[**Иажентусеринпут:: жетитемконфиденце**](iagentuserinput--getitemconfidence.md), [**Иажентусеринпут:: жетитемтекст**](iagentuserinput--getitemtext.md), [**иажентусеринпут:: жетитемид**](iagentuserinput--getitemid.md)</span><span class="sxs-lookup"><span data-stu-id="14215-121">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)</span></span>


 

 




