---
title: Справочник по звуковым микшерам
description: Справочник по звуковым микшерам
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- мультимедиа аудио, аудио миксерс
- аудио, аудио миксерс
- мультимедиа аудио, Справочник по микшерам
- аудио, Справочник по микшерам
- аудио миксерс, Справочник
- миксерс, Справочник
- Справочник по Audio миксерс, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260842"
---
# <a name="audio-mixer-reference"></a><span data-ttu-id="01742-110">Справочник по звуковым микшерам</span><span class="sxs-lookup"><span data-stu-id="01742-110">Audio Mixer Reference</span></span>

<span data-ttu-id="01742-111">В этом разделе описываются функции, структуры и сообщения, связанные с Audio миксерс.</span><span class="sxs-lookup"><span data-stu-id="01742-111">This section describes the functions, structures, and messages associated with audio mixers.</span></span> <span data-ttu-id="01742-112">Эти элементы группируются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="01742-112">These elements are grouped as follows.</span></span>

## <a name="querying-devices"></a><span data-ttu-id="01742-113">Запросы устройств</span><span class="sxs-lookup"><span data-stu-id="01742-113">Querying Devices</span></span>

-   [<span data-ttu-id="01742-114">**миксеркапс**</span><span class="sxs-lookup"><span data-stu-id="01742-114">**MIXERCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [<span data-ttu-id="01742-115">**миксержетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="01742-115">**mixerGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [<span data-ttu-id="01742-116">**миксержетнумдевс**</span><span class="sxs-lookup"><span data-stu-id="01742-116">**mixerGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a><span data-ttu-id="01742-117">Открытие и закрытие</span><span class="sxs-lookup"><span data-stu-id="01742-117">Opening and Closing</span></span>

-   [<span data-ttu-id="01742-118">**миксерклосе**</span><span class="sxs-lookup"><span data-stu-id="01742-118">**mixerClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [<span data-ttu-id="01742-119">**миксеропен**</span><span class="sxs-lookup"><span data-stu-id="01742-119">**mixerOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a><span data-ttu-id="01742-120">Получение идентификаторов микшера</span><span class="sxs-lookup"><span data-stu-id="01742-120">Retrieving Mixer Identifiers</span></span>

-   [<span data-ttu-id="01742-121">**миксержетид**</span><span class="sxs-lookup"><span data-stu-id="01742-121">**mixerGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a><span data-ttu-id="01742-122">Получение элементов управления "линия"</span><span class="sxs-lookup"><span data-stu-id="01742-122">Retrieving Line Controls</span></span>

-   [<span data-ttu-id="01742-123">**миксерконтрол**</span><span class="sxs-lookup"><span data-stu-id="01742-123">**MIXERCONTROL**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [<span data-ttu-id="01742-124">**миксержетлинеконтролс**</span><span class="sxs-lookup"><span data-stu-id="01742-124">**mixerGetLineControls**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [<span data-ttu-id="01742-125">**миксерлинеконтролс**</span><span class="sxs-lookup"><span data-stu-id="01742-125">**MIXERLINECONTROLS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a><span data-ttu-id="01742-126">Изменение атрибутов элемента управления</span><span class="sxs-lookup"><span data-stu-id="01742-126">Changing Control Attributes</span></span>

-   [<span data-ttu-id="01742-127">**миксерконтролдетаилс**</span><span class="sxs-lookup"><span data-stu-id="01742-127">**MIXERCONTROLDETAILS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   <span data-ttu-id="01742-128">[**МИКСЕРКОНТРОЛДЕТАИЛС \_ Boolean**](/previous-versions//dd757295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01742-128">[**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85))</span></span>
-   <span data-ttu-id="01742-129">[**МИКСЕРКОНТРОЛДЕТАИЛС \_ листтекст**](/previous-versions//dd757296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01742-129">[**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span></span>
-   <span data-ttu-id="01742-130">[**МИКСЕРКОНТРОЛДЕТАИЛС \_ подписанный**](/previous-versions//dd757297(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01742-130">[**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85))</span></span>
-   <span data-ttu-id="01742-131">[**МИКСЕРКОНТРОЛДЕТАИЛС \_ без знака**](/previous-versions//dd757298(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01742-131">[**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85))</span></span>
-   [<span data-ttu-id="01742-132">**миксержетконтролдетаилс**</span><span class="sxs-lookup"><span data-stu-id="01742-132">**mixerGetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [<span data-ttu-id="01742-133">**миксерсетконтролдетаилс**</span><span class="sxs-lookup"><span data-stu-id="01742-133">**mixerSetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a><span data-ttu-id="01742-134">Получение сведений о строке</span><span class="sxs-lookup"><span data-stu-id="01742-134">Retrieving Line Information</span></span>

-   [<span data-ttu-id="01742-135">**миксержетлинеинфо**</span><span class="sxs-lookup"><span data-stu-id="01742-135">**mixerGetLineInfo**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [<span data-ttu-id="01742-136">**миксерлине**</span><span class="sxs-lookup"><span data-stu-id="01742-136">**MIXERLINE**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [<span data-ttu-id="01742-137">**\_ \_ изменение элемента управления mm миксм \_**</span><span class="sxs-lookup"><span data-stu-id="01742-137">**MM\_MIXM\_CONTROL\_CHANGE**</span></span>](mm-mixm-control-change.md)
-   [<span data-ttu-id="01742-138">**\_изменение миксм в \_ линии \_ mm**</span><span class="sxs-lookup"><span data-stu-id="01742-138">**MM\_MIXM\_LINE\_CHANGE**</span></span>](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a><span data-ttu-id="01742-139">Отправка сообщений User-Defined</span><span class="sxs-lookup"><span data-stu-id="01742-139">Sending User-Defined Messages</span></span>

-   [<span data-ttu-id="01742-140">**миксермессаже**</span><span class="sxs-lookup"><span data-stu-id="01742-140">**mixerMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a><span data-ttu-id="01742-141">См. также</span><span class="sxs-lookup"><span data-stu-id="01742-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01742-142">Справочник по звуковым микшерам</span><span class="sxs-lookup"><span data-stu-id="01742-142">Audio Mixer Reference</span></span>](audio-mixer-reference.md)
</dt> </dl>

 

 