---
title: Перечисление Вмдвддривеаттачменттипе (Впккоминтерфацес. h)
description: Указывает, что подключено к DVD-дисководу.
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- Перечисление Вмдвддривеаттачменттипе Virtual PC
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c5918fd414a5a83a114ebddf5752647e8db83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491286"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a><span data-ttu-id="cec3e-104">Перечисление Вмдвддривеаттачменттипе</span><span class="sxs-lookup"><span data-stu-id="cec3e-104">VMDVDDriveAttachmentType enumeration</span></span>

<span data-ttu-id="cec3e-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cec3e-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cec3e-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cec3e-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cec3e-107">Указывает, что подключено к DVD-дисководу.</span><span class="sxs-lookup"><span data-stu-id="cec3e-107">Specifies what is attached to a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec3e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cec3e-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="cec3e-109">Константы</span><span class="sxs-lookup"><span data-stu-id="cec3e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cec3e-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**Вмдвддриве \_ None**</span><span class="sxs-lookup"><span data-stu-id="cec3e-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="cec3e-111">Нет присоединенных.</span><span class="sxs-lookup"><span data-stu-id="cec3e-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="cec3e-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**\_изображение вмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="cec3e-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**vmDVDDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="cec3e-113">Имеется прикрепленный файл ISO-образа.</span><span class="sxs-lookup"><span data-stu-id="cec3e-113">There is an ISO image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="cec3e-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**Вмдвддриве \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="cec3e-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="cec3e-115">Подключенный компакт-диск или DVD-дисковод.</span><span class="sxs-lookup"><span data-stu-id="cec3e-115">There is a host CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cec3e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cec3e-116">Requirements</span></span>



| <span data-ttu-id="cec3e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cec3e-117">Requirement</span></span> | <span data-ttu-id="cec3e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cec3e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec3e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cec3e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cec3e-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cec3e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cec3e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cec3e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cec3e-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cec3e-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cec3e-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cec3e-123">End of client support</span></span><br/>    | <span data-ttu-id="cec3e-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cec3e-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cec3e-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="cec3e-125">Product</span></span><br/>                  | <span data-ttu-id="cec3e-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cec3e-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cec3e-127">Header</span><span class="sxs-lookup"><span data-stu-id="cec3e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cec3e-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="cec3e-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec3e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cec3e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec3e-130">**Ивмдвддриве:: вложение**</span><span class="sxs-lookup"><span data-stu-id="cec3e-130">**IVMDVDDrive::Attachment**</span></span>](ivmdvddrive-attachment.md)
</dt> </dl>

 

