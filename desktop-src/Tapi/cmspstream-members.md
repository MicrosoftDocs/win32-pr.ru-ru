---
description: В следующем списке содержатся элементы Кмспстреам.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Элементы Кмспстреам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156566"
---
# <a name="cmspstream-members"></a><span data-ttu-id="bcbab-103">Элементы Кмспстреам</span><span class="sxs-lookup"><span data-stu-id="bcbab-103">CMSPStream Members</span></span>



| <span data-ttu-id="bcbab-104">Тип члена</span><span class="sxs-lookup"><span data-stu-id="bcbab-104">Member type</span></span>                     | <span data-ttu-id="bcbab-105">Имя</span><span class="sxs-lookup"><span data-stu-id="bcbab-105">Name</span></span>                | <span data-ttu-id="bcbab-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bcbab-106">Description</span></span>                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbab-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="bcbab-107">IUnknown</span></span>                        | <span data-ttu-id="bcbab-108">\*m \_ пфтм</span><span class="sxs-lookup"><span data-stu-id="bcbab-108">\*m\_pFTM</span></span>           | <span data-ttu-id="bcbab-109">Указатель на свободный потоковый маршалинг.</span><span class="sxs-lookup"><span data-stu-id="bcbab-109">Pointer to the free threaded marshaller.</span></span>                                                                                                   |
| <span data-ttu-id="bcbab-110">DWORD</span><span class="sxs-lookup"><span data-stu-id="bcbab-110">DWORD</span></span>                           | <span data-ttu-id="bcbab-111">m \_ двстате</span><span class="sxs-lookup"><span data-stu-id="bcbab-111">m\_dwState</span></span>          | <span data-ttu-id="bcbab-112">Текущее состояние потока.</span><span class="sxs-lookup"><span data-stu-id="bcbab-112">The current state of the stream.</span></span>                                                                                                           |
| <span data-ttu-id="bcbab-113">HANDLE</span><span class="sxs-lookup"><span data-stu-id="bcbab-113">HANDLE</span></span>                          | <span data-ttu-id="bcbab-114">m \_ хаддресс</span><span class="sxs-lookup"><span data-stu-id="bcbab-114">m\_hAddress</span></span>         | <span data-ttu-id="bcbab-115">Адрес, в котором используется этот поток.</span><span class="sxs-lookup"><span data-stu-id="bcbab-115">The address on which this stream is being used.</span></span>                                                                                            |
| <span data-ttu-id="bcbab-116">DWORD</span><span class="sxs-lookup"><span data-stu-id="bcbab-116">DWORD</span></span>                           | <span data-ttu-id="bcbab-117">m \_ двмедиатипе</span><span class="sxs-lookup"><span data-stu-id="bcbab-117">m\_dwMediaType</span></span>      | <span data-ttu-id="bcbab-118">[**Тип мультимедиа**](tapimediatype--constants.md) этого потока (аудио, видео и т. д.).</span><span class="sxs-lookup"><span data-stu-id="bcbab-118">The [**media type**](tapimediatype--constants.md) of this stream (audio, video, etc.).</span></span>                                                    |
| <span data-ttu-id="bcbab-119">\_направление терминала</span><span class="sxs-lookup"><span data-stu-id="bcbab-119">TERMINAL\_DIRECTION</span></span>             | <span data-ttu-id="bcbab-120">\_направление m</span><span class="sxs-lookup"><span data-stu-id="bcbab-120">m\_Direction</span></span>        | <span data-ttu-id="bcbab-121">[**Направление**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) этого потока (входящего или исходящего).</span><span class="sxs-lookup"><span data-stu-id="bcbab-121">The [**direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) of this stream (incoming or outgoing).</span></span>                                                         |
| <span data-ttu-id="bcbab-122">кмспкаллбасе</span><span class="sxs-lookup"><span data-stu-id="bcbab-122">CMSPCallBase</span></span>                    | <span data-ttu-id="bcbab-123">\*m \_ пмспкалл</span><span class="sxs-lookup"><span data-stu-id="bcbab-123">\*m\_pMSPCall</span></span>       | <span data-ttu-id="bcbab-124">Указатель на объект вызова.</span><span class="sxs-lookup"><span data-stu-id="bcbab-124">Pointer to the call object.</span></span>                                                                                                                |
| <span data-ttu-id="bcbab-125">играфбуилдер</span><span class="sxs-lookup"><span data-stu-id="bcbab-125">IGraphBuilder</span></span>                   | <span data-ttu-id="bcbab-126">\*m \_ пиграфбуилдер</span><span class="sxs-lookup"><span data-stu-id="bcbab-126">\*m\_pIGraphBuilder</span></span> | <span data-ttu-id="bcbab-127">Указатель на интерфейсы объекта Graph.</span><span class="sxs-lookup"><span data-stu-id="bcbab-127">Pointer to graph object interfaces.</span></span>                                                                                                        |
| <span data-ttu-id="bcbab-128">имедиаконтрол</span><span class="sxs-lookup"><span data-stu-id="bcbab-128">IMediaControl</span></span>                   | <span data-ttu-id="bcbab-129">\*m \_ пимедиаконтрол</span><span class="sxs-lookup"><span data-stu-id="bcbab-129">\*m\_pIMediaControl</span></span> | <span data-ttu-id="bcbab-130">Указатель на интерфейс управления мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bcbab-130">Pointer to the media control interface.</span></span>                                                                                                    |
| <span data-ttu-id="bcbab-131">Кмспаррай <Иттерминал \*></span><span class="sxs-lookup"><span data-stu-id="bcbab-131">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="bcbab-132">m \_ терминалов</span><span class="sxs-lookup"><span data-stu-id="bcbab-132">m\_Terminals</span></span>        | <span data-ttu-id="bcbab-133">Список терминалов в потоке.</span><span class="sxs-lookup"><span data-stu-id="bcbab-133">The list of terminals on the stream.</span></span>                                                                                                       |
| <span data-ttu-id="bcbab-134">кмспкритсектион</span><span class="sxs-lookup"><span data-stu-id="bcbab-134">CMSPCritSection</span></span>                 | <span data-ttu-id="bcbab-135">\_Блокировка m</span><span class="sxs-lookup"><span data-stu-id="bcbab-135">m\_lock</span></span>             | <span data-ttu-id="bcbab-136">Блокировка, защищающая объект потока.</span><span class="sxs-lookup"><span data-stu-id="bcbab-136">The lock that protects the stream object.</span></span> <span data-ttu-id="bcbab-137">Объект потока никогда не должен получить блокировку, а затем вызвать метод Мспкалл, который может блокироваться.</span><span class="sxs-lookup"><span data-stu-id="bcbab-137">The stream object should never acquire the lock and then call an MSPCall method that might lock.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bcbab-138">См. также</span><span class="sxs-lookup"><span data-stu-id="bcbab-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcbab-139">**кмспстреам**</span><span class="sxs-lookup"><span data-stu-id="bcbab-139">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



