---
title: Перечисление Вмхарддисктипе (Впккоминтерфацес. h)
description: Указывает тип образа жесткого диска.
ms.assetid: 14480bad-523a-40d8-a6ba-9ec31fe4b217
keywords:
- Перечисление Вмхарддисктипе Virtual PC
topic_type:
- apiref
api_name:
- VMHardDiskType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b59fed6577aa957bae960f7af65be766a03c727e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691888"
---
# <a name="vmharddisktype-enumeration"></a><span data-ttu-id="2b845-104">Перечисление Вмхарддисктипе</span><span class="sxs-lookup"><span data-stu-id="2b845-104">VMHardDiskType enumeration</span></span>

<span data-ttu-id="2b845-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2b845-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2b845-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2b845-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2b845-107">Указывает тип образа жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="2b845-107">Specifies the hard disk image type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b845-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b845-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDiskType_Dynamic       = 0,
  vmDiskType_FixedSize     = 1,
  vmDiskType_Differencing  = 2
} VMHardDiskType;
```



## <a name="constants"></a><span data-ttu-id="2b845-109">Константы</span><span class="sxs-lookup"><span data-stu-id="2b845-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2b845-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**Вмдисктипе \_ dynamic**</span><span class="sxs-lookup"><span data-stu-id="2b845-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType\_Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="2b845-111">Динамически расширяемый образ жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="2b845-111">A dynamically expanding hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="2b845-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**Вмдисктипе \_ FixedSize**</span><span class="sxs-lookup"><span data-stu-id="2b845-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType\_FixedSize**</span></span>
</dt> <dd>

<span data-ttu-id="2b845-113">Образ жесткого диска фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="2b845-113">A fixed-size hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="2b845-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**\_разностное вмдисктипе**</span><span class="sxs-lookup"><span data-stu-id="2b845-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**vmDiskType\_Differencing**</span></span>
</dt> <dd>

<span data-ttu-id="2b845-115">Образ разностного жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="2b845-115">A differencing hard disk image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b845-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2b845-116">Requirements</span></span>



| <span data-ttu-id="2b845-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2b845-117">Requirement</span></span> | <span data-ttu-id="2b845-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2b845-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b845-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b845-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2b845-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2b845-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b845-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b845-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2b845-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2b845-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2b845-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2b845-123">End of client support</span></span><br/>    | <span data-ttu-id="2b845-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b845-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2b845-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="2b845-125">Product</span></span><br/>                  | <span data-ttu-id="2b845-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2b845-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2b845-127">Header</span><span class="sxs-lookup"><span data-stu-id="2b845-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b845-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b845-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b845-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b845-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b845-130">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="2b845-130">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

