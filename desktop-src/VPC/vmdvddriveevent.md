---
title: Перечисление Вмдвддрививент (Впккоминтерфацес. h)
description: Указывает события DVD-дисковода.
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- Перечисление Вмдвддрививент Virtual PC
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967fcd545c0ddd24d01c5dc779929ef4639c6736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802195"
---
# <a name="vmdvddriveevent-enumeration"></a><span data-ttu-id="58e74-104">Перечисление Вмдвддрививент</span><span class="sxs-lookup"><span data-stu-id="58e74-104">VMDVDDriveEvent enumeration</span></span>

<span data-ttu-id="58e74-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="58e74-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="58e74-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="58e74-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="58e74-107">Указывает события DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="58e74-107">Specifies the DVD drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e74-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58e74-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="58e74-109">Константы</span><span class="sxs-lookup"><span data-stu-id="58e74-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="58e74-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**Вмдвддрививент \_ INSERT**</span><span class="sxs-lookup"><span data-stu-id="58e74-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="58e74-111">Прикрепленный ISO-образ или реальный носитель вставляется в диск узла.</span><span class="sxs-lookup"><span data-stu-id="58e74-111">An ISO image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="58e74-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**Вмдвддрививент \_**</span><span class="sxs-lookup"><span data-stu-id="58e74-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="58e74-113">Носитель был извлечен.</span><span class="sxs-lookup"><span data-stu-id="58e74-113">The media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58e74-114">Требования</span><span class="sxs-lookup"><span data-stu-id="58e74-114">Requirements</span></span>



| <span data-ttu-id="58e74-115">Требование</span><span class="sxs-lookup"><span data-stu-id="58e74-115">Requirement</span></span> | <span data-ttu-id="58e74-116">Значение</span><span class="sxs-lookup"><span data-stu-id="58e74-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e74-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58e74-117">Minimum supported client</span></span><br/> | <span data-ttu-id="58e74-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="58e74-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58e74-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58e74-119">Minimum supported server</span></span><br/> | <span data-ttu-id="58e74-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="58e74-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="58e74-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="58e74-121">End of client support</span></span><br/>    | <span data-ttu-id="58e74-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="58e74-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="58e74-123">Продукт</span><span class="sxs-lookup"><span data-stu-id="58e74-123">Product</span></span><br/>                  | <span data-ttu-id="58e74-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="58e74-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="58e74-125">Header</span><span class="sxs-lookup"><span data-stu-id="58e74-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="58e74-126"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="58e74-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e74-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58e74-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e74-128">**ивмдвддрививентс**</span><span class="sxs-lookup"><span data-stu-id="58e74-128">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

