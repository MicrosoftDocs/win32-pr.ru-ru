---
title: Структура MPSCAN_RESOURCES (Мпклиент. h)
description: Сведения о ресурсах, переданные во время операции просмотра.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES структуры устаревшие функции среды Windows
- Функции PMPSCAN_RESOURCES указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989382"
---
# <a name="mpscan_resources-structure"></a><span data-ttu-id="6d1a9-105">\_Структура ресурсов мпскан</span><span class="sxs-lookup"><span data-stu-id="6d1a9-105">MPSCAN\_RESOURCES structure</span></span>

<span data-ttu-id="6d1a9-106">Сведения о ресурсах, переданные во время операции просмотра.</span><span class="sxs-lookup"><span data-stu-id="6d1a9-106">Resource information passed during a scan operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d1a9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d1a9-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a><span data-ttu-id="6d1a9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6d1a9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d1a9-109">**двресаурцекаунт**</span><span class="sxs-lookup"><span data-stu-id="6d1a9-109">**dwResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="6d1a9-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6d1a9-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6d1a9-111">Число ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d1a9-111">Count of resources.</span></span>

</dd> <dt>

<span data-ttu-id="6d1a9-112">**пресаурцелист**</span><span class="sxs-lookup"><span data-stu-id="6d1a9-112">**pResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="6d1a9-113">Тип: **пмпресаурце \_ info** .</span><span class="sxs-lookup"><span data-stu-id="6d1a9-113">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="6d1a9-114">Массив ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d1a9-114">Array of resources.</span></span> <span data-ttu-id="6d1a9-115">См [**. \_ сведения о мпресаурце**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="6d1a9-115">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d1a9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6d1a9-116">Requirements</span></span>



| <span data-ttu-id="6d1a9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6d1a9-117">Requirement</span></span> | <span data-ttu-id="6d1a9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6d1a9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1a9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d1a9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d1a9-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6d1a9-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6d1a9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d1a9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d1a9-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6d1a9-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d1a9-123">Header</span><span class="sxs-lookup"><span data-stu-id="6d1a9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d1a9-124"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d1a9-124"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d1a9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d1a9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1a9-126">**\_сведения о мпресаурце**</span><span class="sxs-lookup"><span data-stu-id="6d1a9-126">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





