---
description: В следующем фрагменте кода показано, как запросить и задать адрес многоадресной рассылки для Конференции.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Получение адреса многоадресной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144371"
---
# <a name="acquiring-a-multicast-address"></a><span data-ttu-id="eefee-103">Получение адреса многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="eefee-103">Acquiring a Multicast Address</span></span>

<span data-ttu-id="eefee-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="eefee-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eefee-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="eefee-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="eefee-106">В следующем фрагменте кода показано, как запросить и задать адрес многоадресной рассылки для Конференции.</span><span class="sxs-lookup"><span data-stu-id="eefee-106">The following code fragment illustrates how to request and set a multicast address for a conference.</span></span>

<span data-ttu-id="eefee-107">В целях простоты этот фрагмент показывает назначение одного адреса многоадресной рассылки одному элементу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="eefee-107">For the sake of simplicity, this fragment shows the assignment of one multicast address to one media item.</span></span> <span data-ttu-id="eefee-108">В действительности выбор области, запроса адреса многоадресной рассылки и назначения будет выполняться для каждого элемента мультимедиа, участвующего в Конференции.</span><span class="sxs-lookup"><span data-stu-id="eefee-108">In actuality, the selection of a scope, the multicast address request, and the assignment will be performed for every media item involved in the conference.</span></span>

<span data-ttu-id="eefee-109">В этом фрагменте предполагается, что [соединение с сервером ILS](connecting-to-an-ils-server.md) уже выполнено.</span><span class="sxs-lookup"><span data-stu-id="eefee-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span> <span data-ttu-id="eefee-110">Приведенные здесь операции будут выполнены в разделе "изменение параметров при необходимости" раздела [Создание объявления конференции](creating-a-conference-announcement.md).</span><span class="sxs-lookup"><span data-stu-id="eefee-110">The operations shown here would be performed in the "Modify the settings if necessary" section of [Creating a Conference Announcement](creating-a-conference-announcement.md).</span></span>


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a><span data-ttu-id="eefee-111">См. также</span><span class="sxs-lookup"><span data-stu-id="eefee-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eefee-112">Многоадресные COM-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="eefee-112">Multicast COM Interfaces</span></span>](multicast-com-interfaces.md)
</dt> <dt>

[<span data-ttu-id="eefee-113">**имкастаддрессаллокатион**</span><span class="sxs-lookup"><span data-stu-id="eefee-113">**IMcastAddressAllocation**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[<span data-ttu-id="eefee-114">**имкастскопе**</span><span class="sxs-lookup"><span data-stu-id="eefee-114">**IMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[<span data-ttu-id="eefee-115">**имкастлеасеинфо**</span><span class="sxs-lookup"><span data-stu-id="eefee-115">**IMcastLeaseInfo**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[<span data-ttu-id="eefee-116">**иенуммкастскопе**</span><span class="sxs-lookup"><span data-stu-id="eefee-116">**IEnumMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[<span data-ttu-id="eefee-117">**итконференцеблоб**</span><span class="sxs-lookup"><span data-stu-id="eefee-117">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="eefee-118">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="eefee-118">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="eefee-119">**итмедиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="eefee-119">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="eefee-120">**иенумбстр**</span><span class="sxs-lookup"><span data-stu-id="eefee-120">**IEnumBstr**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[<span data-ttu-id="eefee-121">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="eefee-121">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="eefee-122">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="eefee-122">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 



