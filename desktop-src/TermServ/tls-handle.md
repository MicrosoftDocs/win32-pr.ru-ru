---
title: TLS_HANDLE
description: Представляет маркер сервера лицензий удаленный рабочий стол.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801685"
---
# <a name="tls_handle"></a><span data-ttu-id="96d32-104">\_маркер TLS</span><span class="sxs-lookup"><span data-stu-id="96d32-104">TLS\_HANDLE</span></span>

<span data-ttu-id="96d32-105">Представляет маркер сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="96d32-105">Represents a handle to a Remote Desktop license server.</span></span> <span data-ttu-id="96d32-106">Этот маркер возвращается функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="96d32-106">This handle is returned by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="96d32-107">Этот тип данных не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="96d32-107">This data type has no associated header file.</span></span> <span data-ttu-id="96d32-108">Чтобы использовать его, необходимо определить его самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="96d32-108">To use it, you must define it yourself as shown in this topic.</span></span>

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="96d32-109">Требования</span><span class="sxs-lookup"><span data-stu-id="96d32-109">Requirements</span></span>



| <span data-ttu-id="96d32-110">Требование</span><span class="sxs-lookup"><span data-stu-id="96d32-110">Requirement</span></span> | <span data-ttu-id="96d32-111">Значение</span><span class="sxs-lookup"><span data-stu-id="96d32-111">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="96d32-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96d32-112">Minimum supported client</span></span><br/> | <span data-ttu-id="96d32-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96d32-113">Windows Vista</span></span><br/>       |
| <span data-ttu-id="96d32-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96d32-114">Minimum supported server</span></span><br/> | <span data-ttu-id="96d32-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96d32-115">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96d32-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96d32-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d32-117">**тлсконнекттолссервер**</span><span class="sxs-lookup"><span data-stu-id="96d32-117">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="96d32-118">**тлсдисконнектфромсервер**</span><span class="sxs-lookup"><span data-stu-id="96d32-118">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





