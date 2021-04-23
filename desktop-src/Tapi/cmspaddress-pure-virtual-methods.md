---
description: Эти методы должны быть переопределены производными классами.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Чистые виртуальные методы Кмспаддресс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683472"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="c1b1f-103">Чистые виртуальные методы Кмспаддресс</span><span class="sxs-lookup"><span data-stu-id="c1b1f-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="c1b1f-104">Эти методы должны быть переопределены производными классами.</span><span class="sxs-lookup"><span data-stu-id="c1b1f-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="c1b1f-105">Чистые виртуальные методы Кмспаддресс</span><span class="sxs-lookup"><span data-stu-id="c1b1f-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="c1b1f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c1b1f-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1b1f-107">**мспаддрессаддреф**</span><span class="sxs-lookup"><span data-stu-id="c1b1f-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="c1b1f-108">Частный метод AddRef для адреса.</span><span class="sxs-lookup"><span data-stu-id="c1b1f-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="c1b1f-109">**мспаддрессрелеасе**</span><span class="sxs-lookup"><span data-stu-id="c1b1f-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="c1b1f-110">Частный метод освобождения для адреса.</span><span class="sxs-lookup"><span data-stu-id="c1b1f-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="c1b1f-111">**креатемспкалл**</span><span class="sxs-lookup"><span data-stu-id="c1b1f-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="c1b1f-112">Вызывается TAPI для создания объекта вызова.</span><span class="sxs-lookup"><span data-stu-id="c1b1f-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="c1b1f-113">Реализация в производном классе должна просто вызывать функцию [**креатемспкаллхелпер**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="c1b1f-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="c1b1f-114">**шутдовнмспкалл**</span><span class="sxs-lookup"><span data-stu-id="c1b1f-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="c1b1f-115">Вызывается TAPI для завершения работы объекта вызова.</span><span class="sxs-lookup"><span data-stu-id="c1b1f-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="c1b1f-116">Реализация в производном классе должна просто вызывать функцию [**шутдовнмспкаллхелпер**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="c1b1f-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="c1b1f-117">**жеткаллмедиатипес**</span><span class="sxs-lookup"><span data-stu-id="c1b1f-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="c1b1f-118">Возвращает типы носителей, поддерживаемые MSP.</span><span class="sxs-lookup"><span data-stu-id="c1b1f-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="c1b1f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c1b1f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1b1f-120">**кмспаддресс**</span><span class="sxs-lookup"><span data-stu-id="c1b1f-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



