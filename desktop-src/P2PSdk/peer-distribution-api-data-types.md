---
description: API однорангового распространения определяет следующие типы данных.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Типы данных API однорангового распространения
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663318"
---
# <a name="peer-distribution-api-data-types"></a><span data-ttu-id="923e9-103">Типы данных API однорангового распространения</span><span class="sxs-lookup"><span data-stu-id="923e9-103">Peer Distribution API Data Types</span></span>

<span data-ttu-id="923e9-104">API однорангового распространения определяет следующие типы данных.</span><span class="sxs-lookup"><span data-stu-id="923e9-104">The Peer Distribution API defines the following data types.</span></span>


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| <span data-ttu-id="923e9-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="923e9-105">Data type</span></span>                                                                                                                     | <span data-ttu-id="923e9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="923e9-106">Description</span></span>                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="923e9-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_маркер экземпляра для класса, \_**</span><span class="sxs-lookup"><span data-stu-id="923e9-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**PEERDIST\_INSTANCE\_HANDLE**</span></span>          | <span data-ttu-id="923e9-108">Маркер, связанный с экземпляром распространения однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="923e9-108">A handle associated with the Peer Distribution instance.</span></span> <span data-ttu-id="923e9-109">Этот обработчик создается [**пирдистстартуп**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)и используется в большинстве операций распространения одноранговых узлов.</span><span class="sxs-lookup"><span data-stu-id="923e9-109">This handle is created by [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup), and used in most Peer Distribution operations.</span></span><br/>                                          |
| <span data-ttu-id="923e9-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_маркер содержимого для объекта, \_**</span><span class="sxs-lookup"><span data-stu-id="923e9-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**PEERDIST\_CONTENT\_HANDLE**</span></span>             | <span data-ttu-id="923e9-111">Маркер, связанный с содержимым.</span><span class="sxs-lookup"><span data-stu-id="923e9-111">A handle associated with content.</span></span> <span data-ttu-id="923e9-112">Этот обработчик создается [**пирдистклиентопенконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) , и на него указывают ссылки при открытии, закрытии, добавлении или публикации содержимого.</span><span class="sxs-lookup"><span data-stu-id="923e9-112">This handle is created by [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) and is referenced when opening, closing, adding, or publishing content.</span></span><br/>                     |
| <span data-ttu-id="923e9-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_Handle контентинфо \_**</span><span class="sxs-lookup"><span data-stu-id="923e9-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**PEERDIST\_CONTENTINFO\_HANDLE**</span></span> | <span data-ttu-id="923e9-114">Маркер, связанный со сведениями о содержимом.</span><span class="sxs-lookup"><span data-stu-id="923e9-114">A handle associated with content information.</span></span> <span data-ttu-id="923e9-115">Этот обработчик создается [**пирдистсерверопенконтентинформатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)и используется при извлечении сведений о кодированном содержимом.</span><span class="sxs-lookup"><span data-stu-id="923e9-115">This handle is created by [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation), and is used when retrieving encoded content information.</span></span><br/> |
| <span data-ttu-id="923e9-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_Handle Stream \_**</span><span class="sxs-lookup"><span data-stu-id="923e9-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**PEERDIST\_STREAM\_HANDLE**</span></span>                | <span data-ttu-id="923e9-117">Маркер, связанный с потоком данных.</span><span class="sxs-lookup"><span data-stu-id="923e9-117">A handle associated with a data stream.</span></span> <span data-ttu-id="923e9-118">Этот маркер создается [**пирдистсерверпублишстреам**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) , и на него указывают ссылки при публикации, закрытии или добавлении в потоковый контент.</span><span class="sxs-lookup"><span data-stu-id="923e9-118">This handle is created by [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) and is referenced when publishing, closing, or adding to streamed content.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="923e9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="923e9-119">Requirements</span></span>



| <span data-ttu-id="923e9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="923e9-120">Requirement</span></span> | <span data-ttu-id="923e9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="923e9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="923e9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="923e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="923e9-123">\[Только для настольных приложений Windows 7 Профессиональная\]</span><span class="sxs-lookup"><span data-stu-id="923e9-123">Windows 7 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="923e9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="923e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="923e9-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="923e9-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="923e9-126">Header</span><span class="sxs-lookup"><span data-stu-id="923e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="923e9-127"><dt>В видеом для. h</dt></span><span class="sxs-lookup"><span data-stu-id="923e9-127"><dt>Peerdist.h</dt></span></span> </dl> |



 

 




