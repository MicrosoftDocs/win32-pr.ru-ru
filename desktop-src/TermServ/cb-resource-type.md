---
title: Перечисление CB_RESOURCE_TYPE (Кбклиент. h)
description: Указывает тип ресурса, к которому подключается входящее подключение.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- Перечисление CB_RESOURCE_TYPE службы удаленных рабочих столов
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801588"
---
# <a name="cb_resource_type-enumeration"></a><span data-ttu-id="849a7-104">\_ \_ Перечисление типов ресурсов CB</span><span class="sxs-lookup"><span data-stu-id="849a7-104">CB\_RESOURCE\_TYPE enumeration</span></span>

<span data-ttu-id="849a7-105">Указывает тип ресурса, к которому подключается входящее подключение.</span><span class="sxs-lookup"><span data-stu-id="849a7-105">Specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="849a7-106">Это перечисление используется со структурой [**\_ \_ сведений о соединении CB**](cb-connection-info.md) .</span><span class="sxs-lookup"><span data-stu-id="849a7-106">This enumeration is used with the [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="849a7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="849a7-107">Syntax</span></span>


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="849a7-108">Константы</span><span class="sxs-lookup"><span data-stu-id="849a7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="849a7-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**ресурс CB не \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="849a7-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB\_RESOURCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="849a7-110">Тип ресурса не определен.</span><span class="sxs-lookup"><span data-stu-id="849a7-110">The resource type is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="849a7-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_сеанс ресурсов \_ CB**</span><span class="sxs-lookup"><span data-stu-id="849a7-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB\_RESOURCE\_SESSION**</span></span>
</dt> <dd>

<span data-ttu-id="849a7-112">Ресурс является удаленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="849a7-112">The resource is a remote session.</span></span>

</dd> <dt>

<span data-ttu-id="849a7-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_ \_ Виртуальная машина ресурса CB**</span><span class="sxs-lookup"><span data-stu-id="849a7-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB\_RESOURCE\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="849a7-114">Ресурс является виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="849a7-114">The resource is a virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="849a7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="849a7-115">Requirements</span></span>



| <span data-ttu-id="849a7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="849a7-116">Requirement</span></span> | <span data-ttu-id="849a7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="849a7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="849a7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="849a7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="849a7-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="849a7-119">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="849a7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="849a7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="849a7-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="849a7-121">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="849a7-122">Header</span><span class="sxs-lookup"><span data-stu-id="849a7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="849a7-123"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="849a7-123"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="849a7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="849a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="849a7-125">**\_ \_ сведения о подключении CB**</span><span class="sxs-lookup"><span data-stu-id="849a7-125">**CB\_CONNECTION\_INFO**</span></span>](cb-connection-info.md)
</dt> </dl>

 

 





