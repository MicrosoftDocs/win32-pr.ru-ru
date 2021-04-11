---
description: В следующем списке содержатся элементы Кмспкаллбасе.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Элементы Кмспкаллбасе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264663"
---
# <a name="cmspcallbase-members"></a><span data-ttu-id="77619-103">Элементы Кмспкаллбасе</span><span class="sxs-lookup"><span data-stu-id="77619-103">CMSPCallBase Members</span></span>



| <span data-ttu-id="77619-104">Тип члена</span><span class="sxs-lookup"><span data-stu-id="77619-104">Member type</span></span>                   | <span data-ttu-id="77619-105">Имя</span><span class="sxs-lookup"><span data-stu-id="77619-105">Name</span></span>             | <span data-ttu-id="77619-106">Описание</span><span class="sxs-lookup"><span data-stu-id="77619-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77619-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="77619-107">IUnknown</span></span>                      | <span data-ttu-id="77619-108">\*m \_ пфтм</span><span class="sxs-lookup"><span data-stu-id="77619-108">\*m\_pFTM</span></span>        | <span data-ttu-id="77619-109">Указатель на свободный потоковый маршалинг.</span><span class="sxs-lookup"><span data-stu-id="77619-109">Pointer to the free threaded marshaller.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="77619-110">кмспаддресс\*</span><span class="sxs-lookup"><span data-stu-id="77619-110">CMSPAddress\*</span></span>                 | <span data-ttu-id="77619-111">\*m \_ пмспаддресс</span><span class="sxs-lookup"><span data-stu-id="77619-111">\*m\_pMSPAddress</span></span> | <span data-ttu-id="77619-112">Указатель на объект адреса MSP.</span><span class="sxs-lookup"><span data-stu-id="77619-112">The pointer to the MSP address object.</span></span> <span data-ttu-id="77619-113">Он используется для получения терминалов по умолчанию, если приложение не выбирает ни одного.</span><span class="sxs-lookup"><span data-stu-id="77619-113">It is used to get the default terminals if the application doesn't select any.</span></span> <span data-ttu-id="77619-114">Он также передает значение refcount (через [**мспаддрессаддреф**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), а не AddRef), чтобы суммарный адрес не выйдет, пока вызов остается активным, но адрес TAPI 3 не аддреф'ед.</span><span class="sxs-lookup"><span data-stu-id="77619-114">It also carries a refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), not AddRef) so that the aggregated address will not go away while the call is still alive, but TAPI 3's address is not AddRef'ed.</span></span> |
| <span data-ttu-id="77619-115">\_обработчик MSP</span><span class="sxs-lookup"><span data-stu-id="77619-115">MSP\_HANDLE</span></span>                   | <span data-ttu-id="77619-116">\*m \_ хткалл</span><span class="sxs-lookup"><span data-stu-id="77619-116">\*m\_htCall</span></span>      | <span data-ttu-id="77619-117">Описатель для вызова TAPI3's.</span><span class="sxs-lookup"><span data-stu-id="77619-117">The handle to TAPI3's call.</span></span> <span data-ttu-id="77619-118">Используется для запуска событий вызова.</span><span class="sxs-lookup"><span data-stu-id="77619-118">Used to fire call events.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="77619-119">DWORD</span><span class="sxs-lookup"><span data-stu-id="77619-119">DWORD</span></span>                         | <span data-ttu-id="77619-120">m \_ двмедиатипе</span><span class="sxs-lookup"><span data-stu-id="77619-120">m\_dwMediaType</span></span>   | <span data-ttu-id="77619-121">Битовая маска типов мультимедиа для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="77619-121">Bitmask of the media types on this call.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="77619-122">Кмспаррай <Итстреам \*></span><span class="sxs-lookup"><span data-stu-id="77619-122">CMSPArray <ITStream \*></span></span> | <span data-ttu-id="77619-123">m \_ потоков</span><span class="sxs-lookup"><span data-stu-id="77619-123">m\_Streams</span></span>       | <span data-ttu-id="77619-124">Список объектов потока в вызове.</span><span class="sxs-lookup"><span data-stu-id="77619-124">The list of stream objects in the call.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="77619-125">кмспкритсектион</span><span class="sxs-lookup"><span data-stu-id="77619-125">CMSPCritSection</span></span>               | <span data-ttu-id="77619-126">\_Блокировка m</span><span class="sxs-lookup"><span data-stu-id="77619-126">m\_lock</span></span>          | <span data-ttu-id="77619-127">Блокировка, защищающая списки потоков.</span><span class="sxs-lookup"><span data-stu-id="77619-127">The lock that protects the stream lists.</span></span>                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="77619-128">См. также</span><span class="sxs-lookup"><span data-stu-id="77619-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77619-129">**кмспкаллбасе**</span><span class="sxs-lookup"><span data-stu-id="77619-129">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



