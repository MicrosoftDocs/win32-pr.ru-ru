---
title: Перечисление Вмфлоппидривеаттачменттипе (Впккоминтерфацес. h)
description: Указывает, что подключено к дисководу гибких дисков.
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- Перечисление Вмфлоппидривеаттачменттипе Virtual PC
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988845"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a><span data-ttu-id="410f3-104">Перечисление Вмфлоппидривеаттачменттипе</span><span class="sxs-lookup"><span data-stu-id="410f3-104">VMFloppyDriveAttachmentType enumeration</span></span>

<span data-ttu-id="410f3-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="410f3-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="410f3-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="410f3-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="410f3-107">Указывает, что подключено к дисководу гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="410f3-107">Specifies what is attached to a floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="410f3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="410f3-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="410f3-109">Константы</span><span class="sxs-lookup"><span data-stu-id="410f3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="410f3-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**Вмфлоппидриве \_ None**</span><span class="sxs-lookup"><span data-stu-id="410f3-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="410f3-111">Нет присоединенных.</span><span class="sxs-lookup"><span data-stu-id="410f3-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="410f3-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**\_изображение вмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="410f3-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmFloppyDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="410f3-113">Файл образа гибкого диска подключен.</span><span class="sxs-lookup"><span data-stu-id="410f3-113">There is a floppy disk image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="410f3-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**Вмфлоппидриве \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="410f3-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="410f3-115">Подключен дисковод гибких дисков узла.</span><span class="sxs-lookup"><span data-stu-id="410f3-115">There is a host floppy drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="410f3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="410f3-116">Requirements</span></span>



| <span data-ttu-id="410f3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="410f3-117">Requirement</span></span> | <span data-ttu-id="410f3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="410f3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="410f3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="410f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="410f3-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="410f3-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="410f3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="410f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="410f3-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="410f3-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="410f3-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="410f3-123">End of client support</span></span><br/>    | <span data-ttu-id="410f3-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="410f3-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="410f3-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="410f3-125">Product</span></span><br/>                  | <span data-ttu-id="410f3-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="410f3-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="410f3-127">Header</span><span class="sxs-lookup"><span data-stu-id="410f3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="410f3-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="410f3-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="410f3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="410f3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410f3-130">**Ивмфлоппидриве:: вложение**</span><span class="sxs-lookup"><span data-stu-id="410f3-130">**IVMFloppyDrive::Attachment**</span></span>](ivmfloppydrive-attachment.md)
</dt> </dl>

 

