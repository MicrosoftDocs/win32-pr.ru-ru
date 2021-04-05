---
title: Перечисление Вмдривебустипе (Впккоминтерфацес. h)
description: Указывает тип шины.
ms.assetid: 7e0926f3-8218-49c9-8d3a-27214c111a77
keywords:
- Перечисление Вмдривебустипе Virtual PC
topic_type:
- apiref
api_name:
- VMDriveBusType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c53b8da4b9c7a6943f083eec62a144dcfb5bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136290"
---
# <a name="vmdrivebustype-enumeration"></a><span data-ttu-id="3e83c-104">Перечисление Вмдривебустипе</span><span class="sxs-lookup"><span data-stu-id="3e83c-104">VMDriveBusType enumeration</span></span>

<span data-ttu-id="3e83c-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e83c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e83c-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e83c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e83c-107">Указывает тип шины.</span><span class="sxs-lookup"><span data-stu-id="3e83c-107">Specifies the type of bus.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e83c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e83c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveBusType_Invalid  = -1,
  vmDriveBusType_IDE      = 0,
  vmDriveBusType_SCSI     = 1
} VMDriveBusType;
```



## <a name="constants"></a><span data-ttu-id="3e83c-109">Константы</span><span class="sxs-lookup"><span data-stu-id="3e83c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3e83c-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**Вмдривебустипе является \_ недопустимым**</span><span class="sxs-lookup"><span data-stu-id="3e83c-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="3e83c-111">Нет типа шины.</span><span class="sxs-lookup"><span data-stu-id="3e83c-111">No bus type.</span></span>

</dd> <dt>

<span data-ttu-id="3e83c-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**\_Интегрированная среда разработки вмдривебустипе**</span><span class="sxs-lookup"><span data-stu-id="3e83c-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmDriveBusType\_IDE**</span></span>
</dt> <dd>

<span data-ttu-id="3e83c-113">Тип шины IDE.</span><span class="sxs-lookup"><span data-stu-id="3e83c-113">IDE bus type.</span></span>

</dd> <dt>

<span data-ttu-id="3e83c-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**Вмдривебустипе \_ SCSI**</span><span class="sxs-lookup"><span data-stu-id="3e83c-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType\_SCSI**</span></span>
</dt> <dd>

<span data-ttu-id="3e83c-115">Тип шины SCSI.</span><span class="sxs-lookup"><span data-stu-id="3e83c-115">SCSI bus type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e83c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3e83c-116">Requirements</span></span>



| <span data-ttu-id="3e83c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3e83c-117">Requirement</span></span> | <span data-ttu-id="3e83c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3e83c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e83c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e83c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e83c-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3e83c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e83c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e83c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e83c-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3e83c-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e83c-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3e83c-123">End of client support</span></span><br/>    | <span data-ttu-id="3e83c-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e83c-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e83c-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="3e83c-125">Product</span></span><br/>                  | <span data-ttu-id="3e83c-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e83c-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e83c-127">Header</span><span class="sxs-lookup"><span data-stu-id="3e83c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e83c-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e83c-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



 

