---
title: Структура WINBIO_BDB_ANSI_381_RECORD (Винбио \_ types. h)
description: Содержит сведения об одном из примеров отпечатка пальца или Palm от конечного пользователя.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- API структуры WINBIO_BDB_ANSI_381_RECORD биометрическая платформа Windows
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414849"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a><span data-ttu-id="f3cc1-104">ВИНБИО \_ БДБ \_ ANSI \_ 381, \_ Структура записи</span><span class="sxs-lookup"><span data-stu-id="f3cc1-104">WINBIO\_BDB\_ANSI\_381\_RECORD structure</span></span>

<span data-ttu-id="f3cc1-105">Структура **\_ записи винбио \_ БДБ \_ ANSI \_ 381** содержит сведения о одном отпечатке пальцев или Palm от конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-105">The **WINBIO\_BDB\_ANSI\_381\_RECORD** structure contains information about a single fingerprint or palm sample from an end user.</span></span> <span data-ttu-id="f3cc1-106">Коллекция этих структур включена в каждую структуру [**\_ \_ \_ \_ заголовков винбио БДБ ANSI 381**](winbio-bdb-ansi-381-header.md) .</span><span class="sxs-lookup"><span data-stu-id="f3cc1-106">A collection of these structures is included in each [**WINBIO\_BDB\_ANSI\_381\_HEADER**](winbio-bdb-ansi-381-header.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3cc1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3cc1-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a><span data-ttu-id="f3cc1-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f3cc1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3cc1-109">**блоккленгс**</span><span class="sxs-lookup"><span data-stu-id="f3cc1-109">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="f3cc1-110">Содержит число байтов в этой структуре плюс число байтов образца данных изображения.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-110">Contains the number of bytes in this structure plus the number of bytes of sample image data.</span></span>

</dd> <dt>

<span data-ttu-id="f3cc1-111">**хоризонталлинеленгс**</span><span class="sxs-lookup"><span data-stu-id="f3cc1-111">**HorizontalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="f3cc1-112">Задает количество пикселей в горизонтальной строке образца.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-112">Specifies the number of pixels in a horizontal line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="f3cc1-113">**вертикаллинеленгс**</span><span class="sxs-lookup"><span data-stu-id="f3cc1-113">**VerticalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="f3cc1-114">Задает количество пикселей в вертикальной строке образца.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-114">Specifies the number of pixels in a vertical line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="f3cc1-115">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="f3cc1-115">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="f3cc1-116">Значение **\_ \_ ПОДтипа БИОметрической метрики винбио** , которое указывает палец или карманный ПК, используемый для создания образца биометрической метрики.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-116">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the finger or palm used to generate the biometric sample.</span></span> <span data-ttu-id="f3cc1-117">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="f3cc1-117">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f3cc1-118">**каунтофвиевс**</span><span class="sxs-lookup"><span data-stu-id="f3cc1-118">**CountOfViews**</span></span>
</dt> <dd>

<span data-ttu-id="f3cc1-119">Необходимо задать один (1);</span><span class="sxs-lookup"><span data-stu-id="f3cc1-119">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="f3cc1-120">**виевнумбер**</span><span class="sxs-lookup"><span data-stu-id="f3cc1-120">**ViewNumber**</span></span>
</dt> <dd>

<span data-ttu-id="f3cc1-121">Необходимо задать один (1);</span><span class="sxs-lookup"><span data-stu-id="f3cc1-121">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="f3cc1-122">**ImageQuality**</span><span class="sxs-lookup"><span data-stu-id="f3cc1-122">**ImageQuality**</span></span>
</dt> <dd>

<span data-ttu-id="f3cc1-123">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-123">Reserved.</span></span> <span data-ttu-id="f3cc1-124">Это должно быть 254 (0xFE).</span><span class="sxs-lookup"><span data-stu-id="f3cc1-124">This must be 254 (0xFE).</span></span>

</dd> <dt>

<span data-ttu-id="f3cc1-125">**импрессионтипе**</span><span class="sxs-lookup"><span data-stu-id="f3cc1-125">**ImpressionType**</span></span>
</dt> <dd>

<span data-ttu-id="f3cc1-126">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-126">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f3cc1-127">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f3cc1-127">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f3cc1-128">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-128">Reserved.</span></span> <span data-ttu-id="f3cc1-129">Значение должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="f3cc1-129">Must be set to zero (0).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3cc1-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3cc1-130">Remarks</span></span>

<span data-ttu-id="f3cc1-131">Элемент « *позиционирование* » указывает область руки или Palm, используемую для создания образца биометрической метрики.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-131">The *Position* member specifies the area of the hand or palm used to make the biometric sample.</span></span> <span data-ttu-id="f3cc1-132">В настоящее время биометрическая платформа Windows (ВБФ) поддерживает только запись отпечатка пальца и использует следующие константы для представления сведений о положении.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-132">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent position information.</span></span>

-   <span data-ttu-id="f3cc1-133">ВИНБИО \_ ANSI \_ 381 \_ POS \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="f3cc1-133">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="f3cc1-134">ВИНБИО \_ ANSI \_ 381 \_ \_ RH POS \_</span><span class="sxs-lookup"><span data-stu-id="f3cc1-134">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="f3cc1-135">ВИНБИО \_ \_ \_ \_ RH \_ указатель \_ пальца ANSI 381 POS</span><span class="sxs-lookup"><span data-stu-id="f3cc1-135">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="f3cc1-136">ВИНБИО \_ ANSI \_ 381 \_ \_ RH, \_ средний \_ палец</span><span class="sxs-lookup"><span data-stu-id="f3cc1-136">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="f3cc1-137">ВИНБИО \_ ANSI \_ 381 \_ POS \_ RH \_ Ring \_</span><span class="sxs-lookup"><span data-stu-id="f3cc1-137">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="f3cc1-138">ВИНБИО \_ ANSI \_ 381 \_ \_ RH, \_ маленький \_ палец</span><span class="sxs-lookup"><span data-stu-id="f3cc1-138">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="f3cc1-139">ВИНБИОный \_ \_ \_ \_ бегунок ANSI 381 POS \_</span><span class="sxs-lookup"><span data-stu-id="f3cc1-139">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="f3cc1-140">ВИНБИОный \_ палец с индексами в формате ANSI \_ 381 \_ POS \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3cc1-140">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="f3cc1-141">\_ \_ Средний палец винбио ANSI 381 \_ POS \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3cc1-141">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="f3cc1-142">ВИНБИОный \_ палец в формате ANSI \_ 381 \_ POS \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3cc1-142">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="f3cc1-143">ВИНБИО \_ ANSI \_ 381 \_ POS \_ , \_ маленький \_ палец</span><span class="sxs-lookup"><span data-stu-id="f3cc1-143">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="f3cc1-144">ВИНБИО \_ ANSI \_ 381 \_ RH POS с \_ \_ четырьмя \_ пальцами</span><span class="sxs-lookup"><span data-stu-id="f3cc1-144">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="f3cc1-145">ВИНБИО \_ ANSI \_ 381 \_ POS \_ LH \_ четыре \_ пальца</span><span class="sxs-lookup"><span data-stu-id="f3cc1-145">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="f3cc1-146">ВИНБИО \_ ANSI \_ 381 \_ POS \_ 2 \_ Thumbs</span><span class="sxs-lookup"><span data-stu-id="f3cc1-146">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f3cc1-147">Не пытайтесь проверить значение, заданное для значения *расположения* .</span><span class="sxs-lookup"><span data-stu-id="f3cc1-147">Do not attempt to validate the value supplied for the *Position* value.</span></span> <span data-ttu-id="f3cc1-148">Служба биометрических систем Windows проверит переданное значение перед его передачей в реализацию.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-148">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="f3cc1-149">Если значение **винбио \_ подтипа \_ нет \_ данных** или **винбио \_ подтип \_ ANY**, то проверьте, где это необходимо.</span><span class="sxs-lookup"><span data-stu-id="f3cc1-149">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3cc1-150">Требования</span><span class="sxs-lookup"><span data-stu-id="f3cc1-150">Requirements</span></span>



| <span data-ttu-id="f3cc1-151">Требование</span><span class="sxs-lookup"><span data-stu-id="f3cc1-151">Requirement</span></span> | <span data-ttu-id="f3cc1-152">Значение</span><span class="sxs-lookup"><span data-stu-id="f3cc1-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3cc1-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3cc1-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f3cc1-154">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f3cc1-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f3cc1-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3cc1-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f3cc1-156">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3cc1-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f3cc1-157">Header</span><span class="sxs-lookup"><span data-stu-id="f3cc1-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3cc1-158"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3cc1-158"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3cc1-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3cc1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3cc1-160">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="f3cc1-160">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





