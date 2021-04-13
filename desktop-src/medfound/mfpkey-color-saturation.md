---
description: Корректирует насыщенность.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: Свойство MFPKEY_COLOR_SATURATION (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544938"
---
# <a name="mfpkey_color_saturation-property"></a><span data-ttu-id="f81ae-103">\_ \_ Свойство насыщенности цвета мфпкэй</span><span class="sxs-lookup"><span data-stu-id="f81ae-103">MFPKEY\_COLOR\_SATURATION Property</span></span>

<span data-ttu-id="f81ae-104">Корректирует насыщенность.</span><span class="sxs-lookup"><span data-stu-id="f81ae-104">Adjusts the saturation.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f81ae-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="f81ae-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f81ae-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f81ae-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f81ae-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f81ae-107">Data Type</span></span>

<span data-ttu-id="f81ae-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f81ae-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f81ae-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f81ae-109">Default Value</span></span>

<span data-ttu-id="f81ae-110">0</span><span class="sxs-lookup"><span data-stu-id="f81ae-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="f81ae-111">Применение</span><span class="sxs-lookup"><span data-stu-id="f81ae-111">Applies To</span></span>

-   [<span data-ttu-id="f81ae-112">Преобразование элемента управления цветом DSP</span><span class="sxs-lookup"><span data-stu-id="f81ae-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="f81ae-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f81ae-113">Remarks</span></span>

<span data-ttu-id="f81ae-114">Корректировка насыщенности выполняется путем умножения значений CB и CR на константу.</span><span class="sxs-lookup"><span data-stu-id="f81ae-114">Saturation adjustment is performed by multiplying the Cb and Cr values by a constant.</span></span>

<span data-ttu-id="f81ae-115">Это свойство имеет диапазон от-127 до 127.</span><span class="sxs-lookup"><span data-stu-id="f81ae-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="f81ae-116">Ноль означает отсутствие изменений в насыщенности.</span><span class="sxs-lookup"><span data-stu-id="f81ae-116">Zero indicates no change in saturation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f81ae-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f81ae-117">Requirements</span></span>



| <span data-ttu-id="f81ae-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f81ae-118">Requirement</span></span> | <span data-ttu-id="f81ae-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f81ae-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f81ae-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f81ae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f81ae-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f81ae-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f81ae-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f81ae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f81ae-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f81ae-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f81ae-124">Header</span><span class="sxs-lookup"><span data-stu-id="f81ae-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f81ae-125"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f81ae-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f81ae-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f81ae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f81ae-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f81ae-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
