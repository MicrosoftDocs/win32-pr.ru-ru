---
title: Перечисление Вмфлоппидрививент (Впккоминтерфацес. h)
description: Указывает события дисковода гибких дисков.
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- Перечисление Вмфлоппидрививент Virtual PC
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b1485f91264713cf96a4f95cab8286261eea4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803460"
---
# <a name="vmfloppydriveevent-enumeration"></a><span data-ttu-id="fd07d-104">Перечисление Вмфлоппидрививент</span><span class="sxs-lookup"><span data-stu-id="fd07d-104">vmFloppyDriveEvent enumeration</span></span>

<span data-ttu-id="fd07d-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd07d-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd07d-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd07d-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd07d-107">Указывает события дисковода гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="fd07d-107">Specifies the floppy drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd07d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd07d-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="fd07d-109">Константы</span><span class="sxs-lookup"><span data-stu-id="fd07d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd07d-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**Вмфлоппидрививент \_ INSERT**</span><span class="sxs-lookup"><span data-stu-id="fd07d-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="fd07d-111">Прикрепленный образ дискеты или реальный носитель вставлен в диск узла.</span><span class="sxs-lookup"><span data-stu-id="fd07d-111">A floppy disk image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="fd07d-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**Вмфлоппидрививент \_**</span><span class="sxs-lookup"><span data-stu-id="fd07d-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="fd07d-113">Носитель был извлечен.</span><span class="sxs-lookup"><span data-stu-id="fd07d-113">Media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd07d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fd07d-114">Requirements</span></span>



| <span data-ttu-id="fd07d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fd07d-115">Requirement</span></span> | <span data-ttu-id="fd07d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fd07d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd07d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd07d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd07d-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd07d-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd07d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd07d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd07d-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd07d-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd07d-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fd07d-121">End of client support</span></span><br/>    | <span data-ttu-id="fd07d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd07d-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd07d-123">Продукт</span><span class="sxs-lookup"><span data-stu-id="fd07d-123">Product</span></span><br/>                  | <span data-ttu-id="fd07d-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd07d-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd07d-125">Header</span><span class="sxs-lookup"><span data-stu-id="fd07d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd07d-126"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd07d-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd07d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd07d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd07d-128">**ивмфлоппидрививентс**</span><span class="sxs-lookup"><span data-stu-id="fd07d-128">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

