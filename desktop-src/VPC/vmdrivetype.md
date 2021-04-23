---
title: Перечисление Вмдриветипе (Впккоминтерфацес. h)
description: Указывает тип диска, подключенного к расположению шины.
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- Перечисление Вмдриветипе Virtual PC
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6001a4a68db51b64eea9bb44d1d4c75863d315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802200"
---
# <a name="vmdrivetype-enumeration"></a><span data-ttu-id="dd923-104">Перечисление Вмдриветипе</span><span class="sxs-lookup"><span data-stu-id="dd923-104">VMDriveType enumeration</span></span>

<span data-ttu-id="dd923-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dd923-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dd923-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dd923-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dd923-107">Указывает тип диска, подключенного к расположению шины.</span><span class="sxs-lookup"><span data-stu-id="dd923-107">Specifies the type of drive attached to a bus location.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd923-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd923-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a><span data-ttu-id="dd923-109">Константы</span><span class="sxs-lookup"><span data-stu-id="dd923-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dd923-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**Вмдриветипе \_ null**</span><span class="sxs-lookup"><span data-stu-id="dd923-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="dd923-111">Нет подключенного диска.</span><span class="sxs-lookup"><span data-stu-id="dd923-111">There is no drive attached.</span></span>

</dd> <dt>

<span data-ttu-id="dd923-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**Вмдриветипе \_ жесткого диска**</span><span class="sxs-lookup"><span data-stu-id="dd923-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType\_HardDisk**</span></span>
</dt> <dd>

<span data-ttu-id="dd923-113">Жесткий диск подключен.</span><span class="sxs-lookup"><span data-stu-id="dd923-113">There is a hard disk attached.</span></span>

</dd> <dt>

<span data-ttu-id="dd923-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**Вмдриветипе \_ DVD**</span><span class="sxs-lookup"><span data-stu-id="dd923-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType\_DVD**</span></span>
</dt> <dd>

<span data-ttu-id="dd923-115">Подключен компакт-диск или DVD-дисковод.</span><span class="sxs-lookup"><span data-stu-id="dd923-115">There is a CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd923-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dd923-116">Requirements</span></span>



| <span data-ttu-id="dd923-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dd923-117">Requirement</span></span> | <span data-ttu-id="dd923-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dd923-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd923-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd923-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dd923-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dd923-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd923-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd923-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dd923-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd923-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dd923-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dd923-123">End of client support</span></span><br/>    | <span data-ttu-id="dd923-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd923-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dd923-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="dd923-125">Product</span></span><br/>                  | <span data-ttu-id="dd923-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dd923-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dd923-127">Header</span><span class="sxs-lookup"><span data-stu-id="dd923-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd923-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd923-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd923-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd923-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd923-130">**Ивмвиртуалмачине:: Аттачеддриветипес**</span><span class="sxs-lookup"><span data-stu-id="dd923-130">**IVMVirtualMachine::AttachedDriveTypes**</span></span>](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

