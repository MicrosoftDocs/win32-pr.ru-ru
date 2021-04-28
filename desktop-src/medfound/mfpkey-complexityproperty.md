---
description: MFPKEY_COMPLEXITY свойство — указывает сложность алгоритма кодировщика.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: Свойство MFPKEY_COMPLEXITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092942"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="bdee3-103">МФПКЭЙ, \_ свойство сложности</span><span class="sxs-lookup"><span data-stu-id="bdee3-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="bdee3-104">\[[**Мфпкэй \_ СЛОЖНОСТЬ**](mfpkey-complexityexproperty.md) доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="bdee3-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bdee3-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="bdee3-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="bdee3-106">Вместо этого используйте **мфпкэй \_ комплекситекс**.\]</span><span class="sxs-lookup"><span data-stu-id="bdee3-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="bdee3-107">Указывает сложность алгоритма кодировщика.</span><span class="sxs-lookup"><span data-stu-id="bdee3-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="bdee3-108">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="bdee3-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="bdee3-109">g \_ всзвмвккомплекситимоде</span><span class="sxs-lookup"><span data-stu-id="bdee3-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="bdee3-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bdee3-110">Data Type</span></span>

<span data-ttu-id="bdee3-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="bdee3-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="bdee3-112">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bdee3-112">Default Value</span></span>

<span data-ttu-id="bdee3-113">Значение по умолчанию зависит от версии кодировщика видео, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bdee3-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="bdee3-114">Версия кодировщика</span><span class="sxs-lookup"><span data-stu-id="bdee3-114">Encoder version</span></span>                 | <span data-ttu-id="bdee3-115">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bdee3-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="bdee3-116">Кодировщик Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="bdee3-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="bdee3-117">3</span><span class="sxs-lookup"><span data-stu-id="bdee3-117">3</span></span>             |
| <span data-ttu-id="bdee3-118">Кодировщик Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="bdee3-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="bdee3-119">1</span><span class="sxs-lookup"><span data-stu-id="bdee3-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="bdee3-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="bdee3-120">Remarks</span></span>

<span data-ttu-id="bdee3-121">Это целое число в диапазоне от 0 до 3.</span><span class="sxs-lookup"><span data-stu-id="bdee3-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="bdee3-122">Более низкие значения приводят к тому, что кодек использует менее сложные алгоритмы кодирования.</span><span class="sxs-lookup"><span data-stu-id="bdee3-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="bdee3-123">Хотя более простые алгоритмы обеспечивают более низкое качество вывода, процесс кодирования выполняется быстрее и требует меньше вычислительной мощности.</span><span class="sxs-lookup"><span data-stu-id="bdee3-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdee3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="bdee3-124">Requirements</span></span>



| <span data-ttu-id="bdee3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="bdee3-125">Requirement</span></span> | <span data-ttu-id="bdee3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="bdee3-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdee3-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdee3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bdee3-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bdee3-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bdee3-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdee3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bdee3-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bdee3-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bdee3-131">Header</span><span class="sxs-lookup"><span data-stu-id="bdee3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdee3-132"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdee3-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdee3-133">См. также</span><span class="sxs-lookup"><span data-stu-id="bdee3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdee3-134">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bdee3-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




