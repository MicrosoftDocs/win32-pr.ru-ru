---
description: ИДЕНТИФИКАТОР устройства — это независимый от приложения идентификатор для конкретного коммуникационного устройства.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Идентификатор устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545463"
---
# <a name="device-identifier"></a><span data-ttu-id="cbc80-103">Идентификатор устройства</span><span class="sxs-lookup"><span data-stu-id="cbc80-103">Device Identifier</span></span>

<span data-ttu-id="cbc80-104">*Идентификатор устройства* — это независимый от приложения идентификатор для конкретного коммуникационного устройства.</span><span class="sxs-lookup"><span data-stu-id="cbc80-104">A *device ID* is an application-independent identifier for a specific communications device.</span></span> <span data-ttu-id="cbc80-105">Обычно это требуется, только если приложению TAPI требуется передать часть обработки, включающую в себя сеанс связи, с функциями другого API.</span><span class="sxs-lookup"><span data-stu-id="cbc80-105">It is typically needed only when a TAPI application needs to hand off part of the processing involving in a communications session to the functions of a different API.</span></span> <span data-ttu-id="cbc80-106">Например, приложения TAPI 2,2 могут не иметь прямого доступа к потоку мультимедиа и могут использовать API Wave.</span><span class="sxs-lookup"><span data-stu-id="cbc80-106">For example, TAPI 2.2 applications may be unable to directly access a media stream and might use the Wave API.</span></span>

<span data-ttu-id="cbc80-107">**Интерфейс TAPI 2. x:** См. [**линежетид**](/windows/win32/api/tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="cbc80-107">**TAPI 2.x:** See [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="cbc80-108">**Интерфейс TAPI 3. x:** См. раздел [**итаддресскапабилитиес:: Get \_ аддресскапабилити**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*аддресскап* ) с параметром [**адреса \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) **AC \_ перманентдевицеид** .</span><span class="sxs-lookup"><span data-stu-id="cbc80-108">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* set to the **AC\_PERMANENTDEVICEID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span></span>

 

 
