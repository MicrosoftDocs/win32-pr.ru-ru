---
description: Указывает, сколько раз в DSP для записи голоса выполняется подавление акустического эха (AES) на остаточном сигнале.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: Свойство MFPKEY_WMAAECMA_FEATR_AES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647225"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a><span data-ttu-id="24919-103">МФПКЭЙ \_ вмааекма \_ феатр \_ AES, свойство</span><span class="sxs-lookup"><span data-stu-id="24919-103">MFPKEY\_WMAAECMA\_FEATR\_AES Property</span></span>

<span data-ttu-id="24919-104">Указывает, сколько раз в DSP для записи голоса выполняется подавление акустического эха (AES) на остаточном сигнале.</span><span class="sxs-lookup"><span data-stu-id="24919-104">Specifies how many times the Voice Capture DSP performs acoustic echo suppression (AES) on the residual signal.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="24919-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="24919-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="24919-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="24919-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="24919-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="24919-107">Data Type</span></span>

<span data-ttu-id="24919-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="24919-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="24919-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="24919-109">Default Value</span></span>

<span data-ttu-id="24919-110">0</span><span class="sxs-lookup"><span data-stu-id="24919-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="24919-111">Применение</span><span class="sxs-lookup"><span data-stu-id="24919-111">Applies To</span></span>

-   [<span data-ttu-id="24919-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="24919-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="24919-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24919-113">Remarks</span></span>

<span data-ttu-id="24919-114">DSP записи голоса могут выполнять алгоритм AES в остаточном сигнале после отмены эха.</span><span class="sxs-lookup"><span data-stu-id="24919-114">The Voice Capture DSP can perform AES on the residual signal after echo cancellation.</span></span> <span data-ttu-id="24919-115">Это свойство может иметь значение 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="24919-115">This property can have the value 0, 1, or 2.</span></span> <span data-ttu-id="24919-116">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="24919-116">The default value is 0.</span></span> <span data-ttu-id="24919-117">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="24919-117">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="24919-118">DSP использует это свойство только в том случае, если включена обработка AEC.</span><span class="sxs-lookup"><span data-stu-id="24919-118">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="24919-119">Требования</span><span class="sxs-lookup"><span data-stu-id="24919-119">Requirements</span></span>



| <span data-ttu-id="24919-120">Требование</span><span class="sxs-lookup"><span data-stu-id="24919-120">Requirement</span></span> | <span data-ttu-id="24919-121">Значение</span><span class="sxs-lookup"><span data-stu-id="24919-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24919-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24919-122">Minimum supported client</span></span><br/> | <span data-ttu-id="24919-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24919-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="24919-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24919-124">Minimum supported server</span></span><br/> | <span data-ttu-id="24919-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24919-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24919-126">Header</span><span class="sxs-lookup"><span data-stu-id="24919-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="24919-127"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="24919-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24919-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24919-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24919-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24919-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="24919-130">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="24919-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
