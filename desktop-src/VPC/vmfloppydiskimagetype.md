---
title: Перечисление Вмфлоппидискимажетипе (Впккоминтерфацес. h)
description: Указывает форматы дискет.
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- Перечисление Вмфлоппидискимажетипе Virtual PC
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20732e46617288602e841a1047db5db30eba5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415504"
---
# <a name="vmfloppydiskimagetype-enumeration"></a><span data-ttu-id="9fd5b-104">Перечисление Вмфлоппидискимажетипе</span><span class="sxs-lookup"><span data-stu-id="9fd5b-104">VMFloppyDiskImageType enumeration</span></span>

<span data-ttu-id="9fd5b-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9fd5b-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9fd5b-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9fd5b-107">Указывает форматы дискет.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-107">Specifies the floppy disk formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd5b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fd5b-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a><span data-ttu-id="9fd5b-109">Константы</span><span class="sxs-lookup"><span data-stu-id="9fd5b-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9fd5b-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**Вмфлоппидискимаже \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5b-111">Неизвестный формат.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-111">Unknown format.</span></span>

</dd> <dt>

<span data-ttu-id="9fd5b-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**Вмфлоппидискимаже \_ ловденсити**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage\_LowDensity**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5b-113">Формат низкой плотности (720K).</span><span class="sxs-lookup"><span data-stu-id="9fd5b-113">A low density format (720K).</span></span>

</dd> <dt>

<span data-ttu-id="9fd5b-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**Вмфлоппидискимаже \_ хигхденсити**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage\_HighDensity**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5b-115">Формат высокой плотности (1,44 МБ).</span><span class="sxs-lookup"><span data-stu-id="9fd5b-115">A high density format (1.44MB).</span></span>

</dd> <dt>

<span data-ttu-id="9fd5b-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**Вмфлоппидискимаже \_ DMF**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmFloppyDiskImage\_DMF**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5b-117">Формат носителя распространения (1.68 МБ).</span><span class="sxs-lookup"><span data-stu-id="9fd5b-117">A distribution media format (1.68Mb).</span></span>

</dd> <dt>

<span data-ttu-id="9fd5b-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**Вмфлоппидискимаже \_ ловденситисинглесидед**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage\_LowDensitySingleSided**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5b-119">Односторонняя формат низкой плотности.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-119">A single-sided low density format.</span></span>

</dd> <dt>

<span data-ttu-id="9fd5b-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**Вмфлоппидискимаже \_ медиумденсити**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage\_MediumDensity**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5b-121">Формат средней плотности (1,2 МБ).</span><span class="sxs-lookup"><span data-stu-id="9fd5b-121">A medium density format (1.2MB).</span></span>

</dd> <dt>

<span data-ttu-id="9fd5b-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**Вмфлоппидискимаже \_ хигхденситимсс**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage\_HighDensityMSS**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5b-123">Высокоплотный размер сектора (MSS), используемый расширенным форматом распределения (Xdf-).</span><span class="sxs-lookup"><span data-stu-id="9fd5b-123">A high-density Multiple Sector Size (MSS), used by eXtended Distribution Format (XDF).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fd5b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9fd5b-124">Requirements</span></span>



| <span data-ttu-id="9fd5b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9fd5b-125">Requirement</span></span> | <span data-ttu-id="9fd5b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9fd5b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd5b-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fd5b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd5b-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9fd5b-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9fd5b-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fd5b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd5b-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9fd5b-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9fd5b-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9fd5b-131">End of client support</span></span><br/>    | <span data-ttu-id="9fd5b-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9fd5b-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9fd5b-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="9fd5b-133">Product</span></span><br/>                  | <span data-ttu-id="9fd5b-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9fd5b-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9fd5b-135">Header</span><span class="sxs-lookup"><span data-stu-id="9fd5b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fd5b-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd5b-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd5b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fd5b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd5b-138">**Ивмвиртуалпк:: Креатефлоппидискимаже**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-138">**IVMVirtualPC::CreateFloppyDiskImage**</span></span>](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[<span data-ttu-id="9fd5b-139">**Ивмвиртуалпк:: Жетфлоппидискимажетипе**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-139">**IVMVirtualPC::GetFloppyDiskImageType**</span></span>](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

