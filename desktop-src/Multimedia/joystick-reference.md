---
title: Справочник по джойстику
description: Справочник по джойстику
ms.assetid: c2ad092f-a0c5-4e28-ada7-227dc52c3c83
keywords:
- Мультимедиа Windows, Справочник по джойстику
- мультимедиа, Справочник по джойстику
- Ввод мультимедиа, Справочник по джойстику
- Джойстики, справочные материалы
- Справочник по джойстикам, сведения
- Справочник по джойстику, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242f3fb21f9da9b1853ae8e9e7f694b9ad3bf711
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890493"
---
# <a name="joystick-reference"></a><span data-ttu-id="4e07f-109">Справочник по джойстику</span><span class="sxs-lookup"><span data-stu-id="4e07f-109">Joystick Reference</span></span>

<span data-ttu-id="4e07f-110">В этом разделе описываются функции, структуры и сообщения, связанные с джойстиками.</span><span class="sxs-lookup"><span data-stu-id="4e07f-110">This section describes the functions, structures, and messages associated with joysticks.</span></span> <span data-ttu-id="4e07f-111">Элементы группируются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e07f-111">The elements are grouped as follows:</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="4e07f-112">Возможности устройства</span><span class="sxs-lookup"><span data-stu-id="4e07f-112">Device Capabilities</span></span>

-   [<span data-ttu-id="4e07f-113">**жойжетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="4e07f-113">**joyGetDevCaps**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)
-   [<span data-ttu-id="4e07f-114">**жойжетнумдевс**</span><span class="sxs-lookup"><span data-stu-id="4e07f-114">**joyGetNumDevs**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs)
-   [<span data-ttu-id="4e07f-115">**жойкапс**</span><span class="sxs-lookup"><span data-stu-id="4e07f-115">**JOYCAPS**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joycaps)

## <a name="querying-a-joystick"></a><span data-ttu-id="4e07f-116">Запрос к джойстику</span><span class="sxs-lookup"><span data-stu-id="4e07f-116">Querying a Joystick</span></span>

-   [<span data-ttu-id="4e07f-117">**жойконфигчанжед**</span><span class="sxs-lookup"><span data-stu-id="4e07f-117">**joyConfigChanged**</span></span>](/windows/desktop/api/joystickapi/nf-joystickapi-joyconfigchanged)
-   [<span data-ttu-id="4e07f-118">**жойжетпос**</span><span class="sxs-lookup"><span data-stu-id="4e07f-118">**joyGetPos**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos)
-   [<span data-ttu-id="4e07f-119">**жойжетпосекс**</span><span class="sxs-lookup"><span data-stu-id="4e07f-119">**joyGetPosEx**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex)
-   [<span data-ttu-id="4e07f-120">**жойинфо**</span><span class="sxs-lookup"><span data-stu-id="4e07f-120">**JOYINFO**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfo)
-   [<span data-ttu-id="4e07f-121">**жойинфоекс**</span><span class="sxs-lookup"><span data-stu-id="4e07f-121">**JOYINFOEX**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfoex)

## <a name="capturing-a-joystick"></a><span data-ttu-id="4e07f-122">Захват джойстика</span><span class="sxs-lookup"><span data-stu-id="4e07f-122">Capturing a Joystick</span></span>

-   [<span data-ttu-id="4e07f-123">**жойжетсрешолд**</span><span class="sxs-lookup"><span data-stu-id="4e07f-123">**joyGetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetthreshold)
-   [<span data-ttu-id="4e07f-124">**жойрелеасекаптуре**</span><span class="sxs-lookup"><span data-stu-id="4e07f-124">**joyReleaseCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture)
-   [<span data-ttu-id="4e07f-125">**жойсеткаптуре**</span><span class="sxs-lookup"><span data-stu-id="4e07f-125">**joySetCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture)
-   [<span data-ttu-id="4e07f-126">**жойсетсрешолд**</span><span class="sxs-lookup"><span data-stu-id="4e07f-126">**joySetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold)
-   [<span data-ttu-id="4e07f-127">**\_JOY1BUTTONDOWN мм**</span><span class="sxs-lookup"><span data-stu-id="4e07f-127">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md)
-   [<span data-ttu-id="4e07f-128">**\_JOY1BUTTONUP мм**</span><span class="sxs-lookup"><span data-stu-id="4e07f-128">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)
-   [<span data-ttu-id="4e07f-129">**\_JOY1MOVE мм**</span><span class="sxs-lookup"><span data-stu-id="4e07f-129">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)
-   [<span data-ttu-id="4e07f-130">**\_JOY1ZMOVE мм**</span><span class="sxs-lookup"><span data-stu-id="4e07f-130">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)
-   [<span data-ttu-id="4e07f-131">**\_JOY2BUTTONDOWN мм**</span><span class="sxs-lookup"><span data-stu-id="4e07f-131">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md)
-   [<span data-ttu-id="4e07f-132">**\_JOY2BUTTONUP мм**</span><span class="sxs-lookup"><span data-stu-id="4e07f-132">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)
-   [<span data-ttu-id="4e07f-133">**\_JOY2MOVE мм**</span><span class="sxs-lookup"><span data-stu-id="4e07f-133">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)
-   [<span data-ttu-id="4e07f-134">**\_JOY2ZMOVE мм**</span><span class="sxs-lookup"><span data-stu-id="4e07f-134">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)

## <a name="related-topics"></a><span data-ttu-id="4e07f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="4e07f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e07f-136">Джойстики</span><span class="sxs-lookup"><span data-stu-id="4e07f-136">Joysticks</span></span>](joysticks.md)
</dt> </dl>

 

 