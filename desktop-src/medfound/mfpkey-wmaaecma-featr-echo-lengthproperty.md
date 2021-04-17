---
description: Указывает продолжительность эхо-запроса, который алгоритм AEC может обрабатывать (в миллисекундах).
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: Свойство MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692604"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a><span data-ttu-id="5f337-103">МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Длина эхо</span><span class="sxs-lookup"><span data-stu-id="5f337-103">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH Property</span></span>

<span data-ttu-id="5f337-104">Указывает продолжительность эхо-запроса, который алгоритм AEC может обрабатывать (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="5f337-104">Specifies the duration of echo that the acoustic echo cancellation (AEC) algorithm can handle, in milliseconds.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5f337-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="5f337-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5f337-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="5f337-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="5f337-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5f337-107">Data Type</span></span>

<span data-ttu-id="5f337-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5f337-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="5f337-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5f337-109">Default Value</span></span>

<span data-ttu-id="5f337-110">256</span><span class="sxs-lookup"><span data-stu-id="5f337-110">256</span></span>

## <a name="applies-to"></a><span data-ttu-id="5f337-111">Применение</span><span class="sxs-lookup"><span data-stu-id="5f337-111">Applies To</span></span>

-   [<span data-ttu-id="5f337-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="5f337-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="5f337-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f337-113">Remarks</span></span>

<span data-ttu-id="5f337-114">Алгоритм AEC использует адаптивный фильтр, длина которого определяется длительностью эха.</span><span class="sxs-lookup"><span data-stu-id="5f337-114">The AEC algorithm uses an adaptive filter whose length is determined by the duration of the echo.</span></span> <span data-ttu-id="5f337-115">Рекомендуется, чтобы приложения использовали одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5f337-115">It is recommended that applications use one of the following values:</span></span>

-   <span data-ttu-id="5f337-116">128</span><span class="sxs-lookup"><span data-stu-id="5f337-116">128</span></span>
-   <span data-ttu-id="5f337-117">256</span><span class="sxs-lookup"><span data-stu-id="5f337-117">256</span></span>
-   <span data-ttu-id="5f337-118">512</span><span class="sxs-lookup"><span data-stu-id="5f337-118">512</span></span>
-   <span data-ttu-id="5f337-119">1024</span><span class="sxs-lookup"><span data-stu-id="5f337-119">1024</span></span>

<span data-ttu-id="5f337-120">Значение по умолчанию — 256 миллисекунд, что достаточно для большинства офисных и домашних сред.</span><span class="sxs-lookup"><span data-stu-id="5f337-120">The default value is 256 milliseconds, which is sufficient for most office and home environments.</span></span> <span data-ttu-id="5f337-121">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="5f337-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="5f337-122">DSP использует это свойство только в том случае, если включена обработка AEC.</span><span class="sxs-lookup"><span data-stu-id="5f337-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f337-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5f337-123">Requirements</span></span>



| <span data-ttu-id="5f337-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5f337-124">Requirement</span></span> | <span data-ttu-id="5f337-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5f337-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f337-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f337-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5f337-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f337-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5f337-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f337-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5f337-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f337-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f337-130">Header</span><span class="sxs-lookup"><span data-stu-id="5f337-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f337-131"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f337-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f337-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f337-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f337-133">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f337-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5f337-134">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="5f337-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
