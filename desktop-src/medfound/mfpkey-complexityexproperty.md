---
description: MFPKEY_COMPLEXITYEX свойство — указывает сложность алгоритма кодировщика.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: Свойство MFPKEY_COMPLEXITYEX (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20579bcf7a06dc11f47cbef6a53629f3a36b48dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087612"
---
# <a name="mfpkey_complexityex-property"></a><span data-ttu-id="a33d7-103">МФПКЭЙ \_ комплекситекс, свойство</span><span class="sxs-lookup"><span data-stu-id="a33d7-103">MFPKEY\_COMPLEXITYEX Property</span></span>

<span data-ttu-id="a33d7-104">Указывает сложность алгоритма кодировщика.</span><span class="sxs-lookup"><span data-stu-id="a33d7-104">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a33d7-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="a33d7-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a33d7-106">g \_ всзвмвккомплекситекс</span><span class="sxs-lookup"><span data-stu-id="a33d7-106">g\_wszWMVCComplexityEx</span></span>

## <a name="data-type"></a><span data-ttu-id="a33d7-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a33d7-107">Data Type</span></span>

<span data-ttu-id="a33d7-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a33d7-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a33d7-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a33d7-109">Default Value</span></span>

<span data-ttu-id="a33d7-110">Значение по умолчанию зависит от версии кодировщика видео, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a33d7-110">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="a33d7-111">Версия кодировщика</span><span class="sxs-lookup"><span data-stu-id="a33d7-111">Encoder version</span></span>                 | <span data-ttu-id="a33d7-112">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a33d7-112">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="a33d7-113">Кодировщик Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a33d7-113">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="a33d7-114">3</span><span class="sxs-lookup"><span data-stu-id="a33d7-114">3</span></span>             |
| <span data-ttu-id="a33d7-115">Кодировщик Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="a33d7-115">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="a33d7-116">1</span><span class="sxs-lookup"><span data-stu-id="a33d7-116">1</span></span>             |



 

## <a name="possible-values"></a><span data-ttu-id="a33d7-117">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a33d7-117">Possible Values</span></span>

<span data-ttu-id="a33d7-118">Возможные значения зависят от версии кодировщика видео, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a33d7-118">The possible values depend on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="a33d7-119">Версия кодировщика</span><span class="sxs-lookup"><span data-stu-id="a33d7-119">Encoder version</span></span>                 | <span data-ttu-id="a33d7-120">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a33d7-120">Possible values</span></span>  |
|---------------------------------|------------------|
| <span data-ttu-id="a33d7-121">Кодировщик Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a33d7-121">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="a33d7-122">0, 1, 2, 3, 4, 5</span><span class="sxs-lookup"><span data-stu-id="a33d7-122">0, 1, 2, 3, 4, 5</span></span> |
| <span data-ttu-id="a33d7-123">Кодировщик Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="a33d7-123">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="a33d7-124">0, 1</span><span class="sxs-lookup"><span data-stu-id="a33d7-124">0, 1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="a33d7-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="a33d7-125">Remarks</span></span>

<span data-ttu-id="a33d7-126">Более низкие значения приводят к тому, что кодек использует менее сложные алгоритмы кодирования.</span><span class="sxs-lookup"><span data-stu-id="a33d7-126">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="a33d7-127">Хотя более простые алгоритмы обеспечивают более низкое качество вывода, процесс кодирования выполняется быстрее и требует меньше вычислительной мощности.</span><span class="sxs-lookup"><span data-stu-id="a33d7-127">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span> <span data-ttu-id="a33d7-128">Это может быть важно при кодировании содержимого из действующего источника, так как кодировщик должен быстро обрабатывать входные данные, чтобы поддерживать источник.</span><span class="sxs-lookup"><span data-stu-id="a33d7-128">This can be important when encoding content from a live source because the encoder must process inputs fast enough to keep up with the source.</span></span>

<span data-ttu-id="a33d7-129">Любое значение, присвоенное этому свойству, будет проигнорировано, если свойство [мфпкэй \_ компрессионоптимизатионтипе](mfpkey-compressionoptimizationtypeproperty.md) имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="a33d7-129">Any value assigned to this property will be ignored if the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property is set to 1.</span></span> <span data-ttu-id="a33d7-130">В этом случае для МФПКЭЙ \_ комплекситекс автоматически устанавливается значение 3.</span><span class="sxs-lookup"><span data-stu-id="a33d7-130">In that case, MFPKEY\_COMPLEXITYEX is automatically set to 3.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33d7-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a33d7-131">Requirements</span></span>



| <span data-ttu-id="a33d7-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a33d7-132">Requirement</span></span> | <span data-ttu-id="a33d7-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a33d7-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a33d7-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a33d7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a33d7-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a33d7-135">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a33d7-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a33d7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a33d7-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a33d7-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a33d7-138">Header</span><span class="sxs-lookup"><span data-stu-id="a33d7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a33d7-139"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a33d7-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33d7-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a33d7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33d7-141">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a33d7-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




