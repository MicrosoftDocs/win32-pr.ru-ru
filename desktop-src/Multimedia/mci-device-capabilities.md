---
title: Возможности устройства MCI
description: Возможности устройства MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- Макрос МЦивндканконфиг
- Макрос МЦивндканежект
- Макрос МЦивндканплай
- Макрос МЦивндканрекорд
- Макрос МЦивндкансаве
- Макрос МЦивндканвиндов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068525"
---
# <a name="mci-device-capabilities"></a><span data-ttu-id="3573d-109">Возможности устройства MCI</span><span class="sxs-lookup"><span data-stu-id="3573d-109">MCI Device Capabilities</span></span>

<span data-ttu-id="3573d-110">МЦивнд содержит следующие макросы, позволяющие запрашивать их возможности на устройствах MCI.</span><span class="sxs-lookup"><span data-stu-id="3573d-110">MCIWnd includes the following macros to let you query MCI devices for their capabilities.</span></span>



| <span data-ttu-id="3573d-111">Макрос</span><span class="sxs-lookup"><span data-stu-id="3573d-111">Macro</span></span>                                      | <span data-ttu-id="3573d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3573d-112">Description</span></span>                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3573d-113">**мЦивндканконфиг**</span><span class="sxs-lookup"><span data-stu-id="3573d-113">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | <span data-ttu-id="3573d-114">Определяет, имеет ли устройство диалоговое окно конфигурации для поддержки нескольких конфигураций, например устройства МЦИАВИ.</span><span class="sxs-lookup"><span data-stu-id="3573d-114">Determines whether a device has a configuration dialog box to support multiple configurations, such as the MCIAVI device.</span></span>                   |
| [<span data-ttu-id="3573d-115">**мЦивндканежект**</span><span class="sxs-lookup"><span data-stu-id="3573d-115">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | <span data-ttu-id="3573d-116">Определяет, имеет ли устройство функцию извлечения, управляемой программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="3573d-116">Determines whether a device has a software-controlled eject function.</span></span>                                                                       |
| [<span data-ttu-id="3573d-117">**мЦивндканплай**</span><span class="sxs-lookup"><span data-stu-id="3573d-117">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | <span data-ttu-id="3573d-118">Определяет, может ли устройство воспроизводить существующее содержимое.</span><span class="sxs-lookup"><span data-stu-id="3573d-118">Determines whether a device can play the existing content.</span></span>                                                                                  |
| [<span data-ttu-id="3573d-119">**мЦивндканрекорд**</span><span class="sxs-lookup"><span data-stu-id="3573d-119">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | <span data-ttu-id="3573d-120">Определяет, может ли устройство записывать.</span><span class="sxs-lookup"><span data-stu-id="3573d-120">Determines whether a device can record.</span></span>                                                                                                     |
| [<span data-ttu-id="3573d-121">**мЦивндкансаве**</span><span class="sxs-lookup"><span data-stu-id="3573d-121">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | <span data-ttu-id="3573d-122">Определяет, может ли устройство хранить данные.</span><span class="sxs-lookup"><span data-stu-id="3573d-122">Determines whether a device can store data.</span></span>                                                                                                 |
| [<span data-ttu-id="3573d-123">**мЦивндканвиндов**</span><span class="sxs-lookup"><span data-stu-id="3573d-123">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | <span data-ttu-id="3573d-124">Определяет, поддерживает ли устройство команды окна MCI (например, [**окно**](window.md), [**Размещение**](put.md) и [**место**](where.md)).</span><span class="sxs-lookup"><span data-stu-id="3573d-124">Determines whether a device supports MCI window commands (such as [**window**](window.md), [**put**](put.md) and [**where**](where.md)).</span></span> |



 

<span data-ttu-id="3573d-125">Эти макросы возвращают **значение true** , если устройство поддерживает определенную возможность, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3573d-125">These macros return **TRUE** if the device supports the specific capability, or **FALSE** otherwise.</span></span>

 

 




