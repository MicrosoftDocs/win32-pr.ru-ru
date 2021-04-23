---
description: Указывает, выполняет ли DSP для записи речи автоматический контроль усиления.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: Свойство MFPKEY_WMAAECMA_FEATR_AGC (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692605"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a><span data-ttu-id="f735a-103">МФПКЭЙ \_ вмааекма \_ феатр \_ АГК, свойство</span><span class="sxs-lookup"><span data-stu-id="f735a-103">MFPKEY\_WMAAECMA\_FEATR\_AGC Property</span></span>

<span data-ttu-id="f735a-104">Указывает, выполняет ли DSP для записи речи автоматический контроль усиления.</span><span class="sxs-lookup"><span data-stu-id="f735a-104">Specifies whether the Voice Capture DSP performs automatic gain control.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f735a-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="f735a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f735a-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f735a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f735a-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f735a-107">Data Type</span></span>

<span data-ttu-id="f735a-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="f735a-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="f735a-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f735a-109">Default Value</span></span>

<span data-ttu-id="f735a-110">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="f735a-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="f735a-111">Применение</span><span class="sxs-lookup"><span data-stu-id="f735a-111">Applies To</span></span>

-   [<span data-ttu-id="f735a-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="f735a-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="f735a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f735a-113">Remarks</span></span>

<span data-ttu-id="f735a-114">Автоматический усиление контроля — это компонент DSP, который корректирует прибыль таким образом, чтобы уровень вывода сигнала оставался в том же приближенном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="f735a-114">Automatic gain control is a digital signal processing (DSP) component that adjusts the gain so that the output level of the signal remains within the same approximate range.</span></span>

<span data-ttu-id="f735a-115">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="f735a-115">This property can have the following values.</span></span>



| <span data-ttu-id="f735a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f735a-116">Value</span></span>          | <span data-ttu-id="f735a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f735a-117">Description</span></span>                     |
|----------------|---------------------------------|
| <span data-ttu-id="f735a-118">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="f735a-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="f735a-119">Отключить автоматический контроль усиления.</span><span class="sxs-lookup"><span data-stu-id="f735a-119">Disable automatic gain control.</span></span> |
| <span data-ttu-id="f735a-120">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="f735a-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="f735a-121">Включить автоматический контроль усиления.</span><span class="sxs-lookup"><span data-stu-id="f735a-121">Enable automatic gain control.</span></span>  |



 

<span data-ttu-id="f735a-122">По умолчанию это свойство имеет значение VARIANT \_ false (отключено).</span><span class="sxs-lookup"><span data-stu-id="f735a-122">The default value of this property is VARIANT\_FALSE (disabled).</span></span> <span data-ttu-id="f735a-123">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="f735a-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="f735a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f735a-124">Requirements</span></span>



| <span data-ttu-id="f735a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f735a-125">Requirement</span></span> | <span data-ttu-id="f735a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f735a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f735a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f735a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f735a-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f735a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f735a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f735a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f735a-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f735a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f735a-131">Header</span><span class="sxs-lookup"><span data-stu-id="f735a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f735a-132"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f735a-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f735a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f735a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f735a-134">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f735a-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f735a-135">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="f735a-135">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
