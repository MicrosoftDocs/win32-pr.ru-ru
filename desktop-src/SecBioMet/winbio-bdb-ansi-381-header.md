---
title: Структура WINBIO_BDB_ANSI_381_HEADER (Винбио \_ types. h)
description: Указывает сведения о ряде образцов отпечатков пальцев или карманных ПК.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- API структуры WINBIO_BDB_ANSI_381_HEADER биометрическая платформа Windows
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681891"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a><span data-ttu-id="6939d-104">ВИНБИО \_ БДБ \_ ANSI \_ 381, \_ структура заголовка</span><span class="sxs-lookup"><span data-stu-id="6939d-104">WINBIO\_BDB\_ANSI\_381\_HEADER structure</span></span>

<span data-ttu-id="6939d-105">В **\_ \_ \_ \_ заголовке винбио БДБ ANSI 381** указаны сведения о ряде образцов отпечатков пальцев или карманных ПК.</span><span class="sxs-lookup"><span data-stu-id="6939d-105">The **WINBIO\_BDB\_ANSI\_381\_HEADER** structure specifies information about a series of fingerprint or palm samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="6939d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6939d-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a><span data-ttu-id="6939d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6939d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6939d-108">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="6939d-108">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-109">Размер (в байтах) этой структуры плюс размер всех структур [**\_ записи винбио бдб \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) для образцов отпечатка и карманного компьютера, полученных от конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="6939d-109">The size, in bytes, of this structure plus the size of all [**WINBIO\_BDB\_ANSI\_381\_RECORD**](winbio-bdb-ansi-381-record.md) structures for the fingerprint or palm samples captured from an end user.</span></span> <span data-ttu-id="6939d-110">Допустимы только младшие шесть байт.</span><span class="sxs-lookup"><span data-stu-id="6939d-110">Only the low six bytes are valid.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-111">**форматидентифиер**</span><span class="sxs-lookup"><span data-stu-id="6939d-111">**FormatIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-112">Задает формат.</span><span class="sxs-lookup"><span data-stu-id="6939d-112">Specifies the format.</span></span> <span data-ttu-id="6939d-113">В настоящее время это должно быть 0x46495200.</span><span class="sxs-lookup"><span data-stu-id="6939d-113">Currently, this must be 0x46495200.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-114">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="6939d-114">**VersionNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-115">Указывает номер версии.</span><span class="sxs-lookup"><span data-stu-id="6939d-115">Specifies the version number.</span></span> <span data-ttu-id="6939d-116">В настоящее время это должно быть 0x30313000, которое соответствует внутреннему 0.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="6939d-116">Currently this must be 0x30313000 which corresponds internally to 0.1.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-117">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="6939d-117">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-118">[**Винбио \_ зарегистрированная структура \_ формата**](winbio-registered-format.md) , которая содержит зарегистрированный формат данных в виде пары "владелец-тип".</span><span class="sxs-lookup"><span data-stu-id="6939d-118">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that contains the registered data format as an owner/type pair.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-119">**каптуредевицеид**</span><span class="sxs-lookup"><span data-stu-id="6939d-119">**CaptureDeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-120">Содержит идентификатор единицы устройства, используемого для записи образца.</span><span class="sxs-lookup"><span data-stu-id="6939d-120">Contains the unit ID of the device used to capture the sample.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-121">**имажеаккуиситионлевел**</span><span class="sxs-lookup"><span data-stu-id="6939d-121">**ImageAcquisitionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-122">Указывает уровень разрешения, на котором захватывается образец.</span><span class="sxs-lookup"><span data-stu-id="6939d-122">Specifies the resolution level at which the sample is captured.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-123">**хоризонталсканресолутион**</span><span class="sxs-lookup"><span data-stu-id="6939d-123">**HorizontalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-124">Задает горизонтальное разрешение сканирования.</span><span class="sxs-lookup"><span data-stu-id="6939d-124">Specifies the horizontal resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-125">**вертикалсканресолутион**</span><span class="sxs-lookup"><span data-stu-id="6939d-125">**VerticalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-126">Задает вертикальное разрешение сканирования.</span><span class="sxs-lookup"><span data-stu-id="6939d-126">Specifies the vertical resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-127">**хоризонталимажересолутион**</span><span class="sxs-lookup"><span data-stu-id="6939d-127">**HorizontalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-128">Задает горизонтальное разрешение захваченного отпечатка или карманного образа.</span><span class="sxs-lookup"><span data-stu-id="6939d-128">Specifies the horizontal resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-129">**вертикалимажересолутион**</span><span class="sxs-lookup"><span data-stu-id="6939d-129">**VerticalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-130">Задает вертикальное разрешение захваченного отпечатка или карманного образа.</span><span class="sxs-lookup"><span data-stu-id="6939d-130">Specifies the vertical resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-131">**ElementCount**</span><span class="sxs-lookup"><span data-stu-id="6939d-131">**ElementCount**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-132">Число записей Finger или Palm в этой структуре.</span><span class="sxs-lookup"><span data-stu-id="6939d-132">Number of finger or palm records in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-133">**Единицы масштабирования**</span><span class="sxs-lookup"><span data-stu-id="6939d-133">**ScaleUnits**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-134">Содержит единицу измерения, 1 для сантиметров и 2 для сантиметров.</span><span class="sxs-lookup"><span data-stu-id="6939d-134">Contains the unit of measure, 1 for inches and 2 for centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-135">**пикселдепс**</span><span class="sxs-lookup"><span data-stu-id="6939d-135">**PixelDepth**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-136">Указывает число битов в пикселе.</span><span class="sxs-lookup"><span data-stu-id="6939d-136">Specifies the number of bits in a pixel.</span></span> <span data-ttu-id="6939d-137">Это может быть от 1 до 16 бит на пиксель для цвета.</span><span class="sxs-lookup"><span data-stu-id="6939d-137">This can be 1 to 16 bits per pixel for color.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-138">**имажекомпрессионалг**</span><span class="sxs-lookup"><span data-stu-id="6939d-138">**ImageCompressionAlg**</span></span>
</dt> <dd>

<span data-ttu-id="6939d-139">Указывает алгоритм, используемый для сжатия изображения пальца или карманного компьютера.</span><span class="sxs-lookup"><span data-stu-id="6939d-139">Specifies the algorithm used to compress the finger or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-140">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="6939d-140">**Reserved**</span></span>
<span data-ttu-id="6939d-141"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6939d-141"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6939d-142">Требования</span><span class="sxs-lookup"><span data-stu-id="6939d-142">Requirements</span></span>



| <span data-ttu-id="6939d-143">Требование</span><span class="sxs-lookup"><span data-stu-id="6939d-143">Requirement</span></span> | <span data-ttu-id="6939d-144">Значение</span><span class="sxs-lookup"><span data-stu-id="6939d-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6939d-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6939d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6939d-146">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6939d-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6939d-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6939d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6939d-148">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6939d-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6939d-149">Header</span><span class="sxs-lookup"><span data-stu-id="6939d-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="6939d-150"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6939d-150"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6939d-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6939d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6939d-152">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="6939d-152">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





