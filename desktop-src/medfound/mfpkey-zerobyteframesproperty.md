---
description: Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: Свойство MFPKEY_ZEROBYTEFRAMES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898201"
---
# <a name="mfpkey_zerobyteframes-property"></a><span data-ttu-id="be6e3-103">МФПКЭЙ \_ зеробитефрамес, свойство</span><span class="sxs-lookup"><span data-stu-id="be6e3-103">MFPKEY\_ZEROBYTEFRAMES Property</span></span>

<span data-ttu-id="be6e3-104">Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.</span><span class="sxs-lookup"><span data-stu-id="be6e3-104">Specifies the number of video frames that are skipped because they were duplicates of previous frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="be6e3-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="be6e3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="be6e3-106">g \_ всзвмвкзеробитефрамес</span><span class="sxs-lookup"><span data-stu-id="be6e3-106">g\_wszWMVCZeroByteFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="be6e3-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="be6e3-107">Data Type</span></span>

<span data-ttu-id="be6e3-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="be6e3-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="be6e3-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be6e3-109">Remarks</span></span>

<span data-ttu-id="be6e3-110">Это значение не вычитается из общего числа переданных кадров ([мфпкэй \_ тоталфрамес](mfpkey-totalframesproperty.md)) при вычислении количества закодированных кадров ([мфпкэй \_ кодедфрамес](mfpkey-codedframesproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="be6e3-110">This value is not subtracted from the total number of frames passed ([MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md)) when calculating the number of encoded frames ([MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md)).</span></span>

<span data-ttu-id="be6e3-111">Вы можете запретить кодеку пропускать дубликаты кадров, установив для [мфпкэй \_ ПРОДУЦЕДУММИФРАМЕС](mfpkey-producedummyframesproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="be6e3-111">You can stop the codec from skipping duplicate frames by setting [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) to VARIANT\_TRUE.</span></span>

<span data-ttu-id="be6e3-112">Это значение можно получить после завершения передачи образцов.</span><span class="sxs-lookup"><span data-stu-id="be6e3-112">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="be6e3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="be6e3-113">Requirements</span></span>



| <span data-ttu-id="be6e3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="be6e3-114">Requirement</span></span> | <span data-ttu-id="be6e3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="be6e3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be6e3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be6e3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="be6e3-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="be6e3-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="be6e3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be6e3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="be6e3-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be6e3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be6e3-120">Header</span><span class="sxs-lookup"><span data-stu-id="be6e3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="be6e3-121"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="be6e3-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be6e3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be6e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6e3-123">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be6e3-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




