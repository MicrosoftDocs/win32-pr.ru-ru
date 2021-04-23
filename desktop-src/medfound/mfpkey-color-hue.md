---
description: Регулирует оттенок.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: Свойство MFPKEY_COLOR_HUE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156098"
---
# <a name="mfpkey_color_hue-property"></a><span data-ttu-id="1c55d-103">\_Свойство цветового \_ тона мфпкэй</span><span class="sxs-lookup"><span data-stu-id="1c55d-103">MFPKEY\_COLOR\_HUE Property</span></span>

<span data-ttu-id="1c55d-104">Регулирует оттенок.</span><span class="sxs-lookup"><span data-stu-id="1c55d-104">Adjusts the hue.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1c55d-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="1c55d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1c55d-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="1c55d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1c55d-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1c55d-107">Data Type</span></span>

<span data-ttu-id="1c55d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1c55d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1c55d-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1c55d-109">Default Value</span></span>

<span data-ttu-id="1c55d-110">0</span><span class="sxs-lookup"><span data-stu-id="1c55d-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="1c55d-111">Применение</span><span class="sxs-lookup"><span data-stu-id="1c55d-111">Applies To</span></span>

-   [<span data-ttu-id="1c55d-112">Преобразование элемента управления цветом DSP</span><span class="sxs-lookup"><span data-stu-id="1c55d-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="1c55d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c55d-113">Remarks</span></span>

<span data-ttu-id="1c55d-114">Корректировка оттенков выполняется путем смешения значений CB и CR.</span><span class="sxs-lookup"><span data-stu-id="1c55d-114">Hue adjustment is performed by mixing the Cb and Cr values.</span></span> <span data-ttu-id="1c55d-115">(Если CB и CR отображаются в двухмерном пространстве, Настройка оттенков выполняется путем поворота вокруг источника.)</span><span class="sxs-lookup"><span data-stu-id="1c55d-115">(If Cb and Cr are plotted in a 2-dimensional space, hue adjustment is performed by rotating around the origin.)</span></span>

<span data-ttu-id="1c55d-116">Это свойство имеет диапазон от-127 до 127.</span><span class="sxs-lookup"><span data-stu-id="1c55d-116">This property has a range of -127 to 127.</span></span> <span data-ttu-id="1c55d-117">Ноль означает отсутствие изменений в оттенках.</span><span class="sxs-lookup"><span data-stu-id="1c55d-117">Zero indicates no change in hue.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c55d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1c55d-118">Requirements</span></span>



| <span data-ttu-id="1c55d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1c55d-119">Requirement</span></span> | <span data-ttu-id="1c55d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1c55d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c55d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c55d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1c55d-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1c55d-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1c55d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c55d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1c55d-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1c55d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c55d-125">Header</span><span class="sxs-lookup"><span data-stu-id="1c55d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c55d-126"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c55d-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c55d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c55d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c55d-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c55d-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
