---
title: Звуковые линии и управляющие запросы
description: Звуковые линии и управляющие запросы
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- мультимедиа аудио, элементы управления микшера
- аудио, элементы управления микшера
- звуковые миксерсы, звуковые линии
- звуковые линии
- аудио миксерс, элементы управления
- миксерс, элементы управления
- миксерс, звуковые строки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789966"
---
# <a name="audio-line-and-control-queries"></a><span data-ttu-id="807b2-110">Звуковые линии и управляющие запросы</span><span class="sxs-lookup"><span data-stu-id="807b2-110">Audio Line and Control Queries</span></span>

<span data-ttu-id="807b2-111">Службы микшера предоставляют функции для определения сведений о звуковых строках, элементах управления звуковых линий и данных управления.</span><span class="sxs-lookup"><span data-stu-id="807b2-111">The mixer services provide functions for determining information about audio lines, audio-line controls, and control details.</span></span> <span data-ttu-id="807b2-112">Службы также предоставляют функции для настройки сведений об элементе управления.</span><span class="sxs-lookup"><span data-stu-id="807b2-112">The services also provide functions for setting control details.</span></span>

<span data-ttu-id="807b2-113">Для получения сведений о указанной звуковой строке можно использовать функцию [**миксержетлинеинфо**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) .</span><span class="sxs-lookup"><span data-stu-id="807b2-113">You can use the [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) function to retrieve information about a specified audio line.</span></span> <span data-ttu-id="807b2-114">Эта функция заполняет структуру [**миксерлине**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) для указанной исходной звуковой строки, конечной звуковой строки или идентификатора строки.</span><span class="sxs-lookup"><span data-stu-id="807b2-114">This function fills the [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) structure for a specified source audio line, destination audio line, or line identifier.</span></span> <span data-ttu-id="807b2-115">Структура включает номер строки назначения, число каналов в звуковой строке, а также короткое и длинное имя для звуковой линии.</span><span class="sxs-lookup"><span data-stu-id="807b2-115">The structure includes the destination line number, the number of channels in the audio line, as well as a short and a long name for the audio line.</span></span>

<span data-ttu-id="807b2-116">Функция [**миксержетлинеконтролс**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) получает общие сведения об одном или нескольких элементах управления, связанных с звуковой линией.</span><span class="sxs-lookup"><span data-stu-id="807b2-116">The [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) function retrieves general information about one or more controls associated with an audio line.</span></span> <span data-ttu-id="807b2-117">Эта функция заполняет структуру [**миксерлинеконтролс**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) сведениями об указанном элементе управления или элементах управления.</span><span class="sxs-lookup"><span data-stu-id="807b2-117">This function fills the [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) structure with information about the specified control or controls.</span></span> <span data-ttu-id="807b2-118">**Миксержетлинеконтролс** можно использовать для получения свойств элемента управления одного из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="807b2-118">You can use **mixerGetLineControls** to retrieve control properties for one of the following:</span></span>

-   <span data-ttu-id="807b2-119">Все элементы управления для указанной исходной строки</span><span class="sxs-lookup"><span data-stu-id="807b2-119">All controls for a specified source line</span></span>
-   <span data-ttu-id="807b2-120">Указанный элемент управления для указанной исходной строки</span><span class="sxs-lookup"><span data-stu-id="807b2-120">A specified control for a specified source line</span></span>
-   <span data-ttu-id="807b2-121">Первый элемент управления определенного класса для указанной исходной строки</span><span class="sxs-lookup"><span data-stu-id="807b2-121">The first control of a specific class for a specified source line</span></span>

<span data-ttu-id="807b2-122">Функция [**миксержетконтролдетаилс**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) извлекает свойства одного элемента управления, связанного с звуковой линией.</span><span class="sxs-lookup"><span data-stu-id="807b2-122">The [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) function retrieves properties of a single control associated with an audio line.</span></span> <span data-ttu-id="807b2-123">Эта функция заполняет структуру [**миксерконтролдетаилс**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) текущими значениями для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="807b2-123">This function fills the [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) structure with the current values for a control.</span></span>

<span data-ttu-id="807b2-124">Функция [**миксерсетконтролдетаилс**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) использует содержимое структуры **миксерконтролдетаилс** для задания свойств указанного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="807b2-124">The [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) function uses the contents of the **MIXERCONTROLDETAILS** structure to set the properties of the specified control.</span></span> <span data-ttu-id="807b2-125">Перед вызовом **миксерсетконтролдетаилс** необходимо убедиться, что все члены этой структуры заполнены.</span><span class="sxs-lookup"><span data-stu-id="807b2-125">You must ensure that all members of this structure are filled before you call **mixerSetControlDetails**.</span></span>

 

 