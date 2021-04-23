---
description: Указывает, как сведения о цвете используются в операциях поиска движения.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: Свойство MFPKEY_MOTIONSEARCHLEVEL (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080610"
---
# <a name="mfpkey_motionsearchlevel-property"></a><span data-ttu-id="f8dec-103">МФПКЭЙ \_ мотионсеарчлевел, свойство</span><span class="sxs-lookup"><span data-stu-id="f8dec-103">MFPKEY\_MOTIONSEARCHLEVEL Property</span></span>

<span data-ttu-id="f8dec-104">Указывает, как сведения о цвете используются в операциях поиска движения.</span><span class="sxs-lookup"><span data-stu-id="f8dec-104">Specifies how color information is used in motion search operations.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f8dec-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="f8dec-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f8dec-106">g \_ всзвмвкмотионсеарчлевел</span><span class="sxs-lookup"><span data-stu-id="f8dec-106">g\_wszWMVCMotionSearchLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="f8dec-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f8dec-107">Data Type</span></span>

<span data-ttu-id="f8dec-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f8dec-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f8dec-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f8dec-109">Default Value</span></span>

<span data-ttu-id="f8dec-110">0</span><span class="sxs-lookup"><span data-stu-id="f8dec-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="f8dec-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8dec-111">Remarks</span></span>

<span data-ttu-id="f8dec-112">Для этого свойства можно задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f8dec-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="f8dec-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f8dec-113">Value</span></span> | <span data-ttu-id="f8dec-114">Сведения об используемом видео</span><span class="sxs-lookup"><span data-stu-id="f8dec-114">Video information used</span></span>                           |
|-------|--------------------------------------------------|
| <span data-ttu-id="f8dec-115">0</span><span class="sxs-lookup"><span data-stu-id="f8dec-115">0</span></span>     | <span data-ttu-id="f8dec-116">Только яркость.</span><span class="sxs-lookup"><span data-stu-id="f8dec-116">Luma only.</span></span>                                       |
| <span data-ttu-id="f8dec-117">1</span><span class="sxs-lookup"><span data-stu-id="f8dec-117">1</span></span>     | <span data-ttu-id="f8dec-118">Яркости с ближайшим целым числом чрома.</span><span class="sxs-lookup"><span data-stu-id="f8dec-118">Luma with nearest-integer chroma.</span></span>                |
| <span data-ttu-id="f8dec-119">2</span><span class="sxs-lookup"><span data-stu-id="f8dec-119">2</span></span>     | <span data-ttu-id="f8dec-120">Яркость с истинной цветностью.</span><span class="sxs-lookup"><span data-stu-id="f8dec-120">Luma with true chroma.</span></span>                           |
| <span data-ttu-id="f8dec-121">-1</span><span class="sxs-lookup"><span data-stu-id="f8dec-121">-1</span></span>    | <span data-ttu-id="f8dec-122">Макроблокк — адаптивный с true чрома.</span><span class="sxs-lookup"><span data-stu-id="f8dec-122">Macroblock-adaptive with true chroma.</span></span>            |
| <span data-ttu-id="f8dec-123">-2</span><span class="sxs-lookup"><span data-stu-id="f8dec-123">-2</span></span>    | <span data-ttu-id="f8dec-124">Макроблокк — адаптивный с ближайшим целым числом чрома.</span><span class="sxs-lookup"><span data-stu-id="f8dec-124">Macroblock-adaptive with nearest-integer chroma.</span></span> |



 

<span data-ttu-id="f8dec-125">По умолчанию кодек выполняет поиск движения только в канале яркости.</span><span class="sxs-lookup"><span data-stu-id="f8dec-125">By default, the codec performs motion search only in the luma channel.</span></span> <span data-ttu-id="f8dec-126">Включение информации чрома в оценку движения может значительно повысить качество закодированного видео.</span><span class="sxs-lookup"><span data-stu-id="f8dec-126">Including chroma information in motion estimation can significantly improve the quality of encoded video.</span></span> <span data-ttu-id="f8dec-127">Поиск движения с помощью яркости и true чрома обеспечит лучшее качество видео, но с наибольшими затратами на производительность.</span><span class="sxs-lookup"><span data-stu-id="f8dec-127">Motion search with luma and true chroma will yield the best video quality, but at the highest performance cost.</span></span> <span data-ttu-id="f8dec-128">Два динамических режима (-1 и-2) и яркости с ближайшим целочисленным режимом чрома обеспечивают разумные компромиссы между качеством и производительностью.</span><span class="sxs-lookup"><span data-stu-id="f8dec-128">The two dynamic modes (-1 and -2) and the luma with nearest-integer chroma mode will provide reasonable compromises between quality and performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8dec-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f8dec-129">Requirements</span></span>



| <span data-ttu-id="f8dec-130">Требование</span><span class="sxs-lookup"><span data-stu-id="f8dec-130">Requirement</span></span> | <span data-ttu-id="f8dec-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f8dec-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8dec-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8dec-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f8dec-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f8dec-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f8dec-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8dec-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f8dec-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8dec-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f8dec-136">Header</span><span class="sxs-lookup"><span data-stu-id="f8dec-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8dec-137"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8dec-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8dec-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8dec-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8dec-139">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f8dec-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




