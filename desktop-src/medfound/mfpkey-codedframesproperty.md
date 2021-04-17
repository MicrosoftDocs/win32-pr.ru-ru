---
description: Указывает число кадров видео, закодированных кодеком.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: Свойство MFPKEY_CODEDFRAMES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663619"
---
# <a name="mfpkey_codedframes-property"></a><span data-ttu-id="b5225-103">МФПКЭЙ \_ кодедфрамес, свойство</span><span class="sxs-lookup"><span data-stu-id="b5225-103">MFPKEY\_CODEDFRAMES Property</span></span>

<span data-ttu-id="b5225-104">Указывает число кадров видео, закодированных кодеком.</span><span class="sxs-lookup"><span data-stu-id="b5225-104">Specifies the number of video frames encoded by the codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b5225-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="b5225-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b5225-106">g \_ всзвмвккодедфрамес</span><span class="sxs-lookup"><span data-stu-id="b5225-106">g\_wszWMVCCodedFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="b5225-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b5225-107">Data Type</span></span>

<span data-ttu-id="b5225-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b5225-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="b5225-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5225-109">Remarks</span></span>

<span data-ttu-id="b5225-110">Это значение равно [мфпкэй \_ тоталфрамес](mfpkey-totalframesproperty.md) минус все кадры, которые были удалены из-за ограничений скорости.</span><span class="sxs-lookup"><span data-stu-id="b5225-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints.</span></span> <span data-ttu-id="b5225-111">Это значение можно получить после завершения передачи образцов.</span><span class="sxs-lookup"><span data-stu-id="b5225-111">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5225-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b5225-112">Requirements</span></span>



| <span data-ttu-id="b5225-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b5225-113">Requirement</span></span> | <span data-ttu-id="b5225-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b5225-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5225-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5225-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b5225-116">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b5225-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b5225-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5225-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b5225-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5225-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5225-119">Header</span><span class="sxs-lookup"><span data-stu-id="b5225-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5225-120"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5225-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5225-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5225-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5225-122">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b5225-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




