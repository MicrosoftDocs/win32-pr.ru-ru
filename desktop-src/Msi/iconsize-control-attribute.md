---
description: Файл значка может содержать несколько различных размеров одного изображения значка.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Атрибут элемента управления Иконсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080673"
---
# <a name="iconsize-control-attribute"></a><span data-ttu-id="10028-103">Атрибут элемента управления Иконсизе</span><span class="sxs-lookup"><span data-stu-id="10028-103">IconSize Control Attribute</span></span>

<span data-ttu-id="10028-104">Файл значка может содержать несколько различных размеров одного изображения значка.</span><span class="sxs-lookup"><span data-stu-id="10028-104">An icon file can hold several different sizes of the same icon image.</span></span> <span data-ttu-id="10028-105">Эти биты указывают, какой размер изображения значка нужно загрузить.</span><span class="sxs-lookup"><span data-stu-id="10028-105">These bits specify which size of the icon image to load.</span></span> <span data-ttu-id="10028-106">Если ни один из битов не задан, будет загружен первый образ.</span><span class="sxs-lookup"><span data-stu-id="10028-106">If none of the bits are set, the first image is loaded.</span></span> <span data-ttu-id="10028-107">Если задано только **msidbControlAttributesIconSize16** , загружается первое изображение 16x16.</span><span class="sxs-lookup"><span data-stu-id="10028-107">If only **msidbControlAttributesIconSize16** is set, the first 16x16 image is loaded.</span></span> <span data-ttu-id="10028-108">Если задан только параметр **msidbControlAttributesIconSize32** , загружается первое изображение размером 32x32.</span><span class="sxs-lookup"><span data-stu-id="10028-108">If only the **msidbControlAttributesIconSize32** is set, the first 32x32 image is loaded.</span></span> <span data-ttu-id="10028-109">Если задано значение **msidbControlAttributesIconSize48** , загружается первое изображение 48x48.</span><span class="sxs-lookup"><span data-stu-id="10028-109">If **msidbControlAttributesIconSize48** is set, the first 48x48 image is loaded.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="10028-110">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="10028-110">Valid Controls</span></span>

[<span data-ttu-id="10028-111">CheckBox</span><span class="sxs-lookup"><span data-stu-id="10028-111">CheckBox</span></span>](checkbox-control.md)

<span data-ttu-id="10028-112">[Значок](icon-control.md):</span><span class="sxs-lookup"><span data-stu-id="10028-112">[Icon](icon-control.md)</span></span>

[<span data-ttu-id="10028-113">PushButton</span><span class="sxs-lookup"><span data-stu-id="10028-113">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="10028-114">радиобуттонграуп</span><span class="sxs-lookup"><span data-stu-id="10028-114">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="10028-115">Значение</span><span class="sxs-lookup"><span data-stu-id="10028-115">Value</span></span>



| <span data-ttu-id="10028-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="10028-116">Decimal</span></span> | <span data-ttu-id="10028-117">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="10028-117">Hexadecimal</span></span> | <span data-ttu-id="10028-118">Описание</span><span class="sxs-lookup"><span data-stu-id="10028-118">Description</span></span>                          |
|---------|-------------|--------------------------------------|
| <span data-ttu-id="10028-119">2097152</span><span class="sxs-lookup"><span data-stu-id="10028-119">2097152</span></span> | <span data-ttu-id="10028-120">0x00200000</span><span class="sxs-lookup"><span data-stu-id="10028-120">0x00200000</span></span>  | <span data-ttu-id="10028-121">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="10028-121">**msidbControlAttributesIconSize16**</span></span> |
| <span data-ttu-id="10028-122">4194304</span><span class="sxs-lookup"><span data-stu-id="10028-122">4194304</span></span> | <span data-ttu-id="10028-123">0x00400000</span><span class="sxs-lookup"><span data-stu-id="10028-123">0x00400000</span></span>  | <span data-ttu-id="10028-124">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="10028-124">**msidbControlAttributesIconSize32**</span></span> |
| <span data-ttu-id="10028-125">6291456</span><span class="sxs-lookup"><span data-stu-id="10028-125">6291456</span></span> | <span data-ttu-id="10028-126">0x00600000</span><span class="sxs-lookup"><span data-stu-id="10028-126">0x00600000</span></span>  | <span data-ttu-id="10028-127">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="10028-127">**msidbControlAttributesIconSize48**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="10028-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10028-128">Remarks</span></span>

<span data-ttu-id="10028-129">Чтобы задать этот атрибут для элемента управления, включите биты Иконсизе в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="10028-129">To set this attribute on a control, include the IconSize bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="10028-130">Если бит [FixedSize](fixedsize-control-attribute.md) не задан, загруженное изображение сжимается или растягивается в соответствии с элементом управления "значок".</span><span class="sxs-lookup"><span data-stu-id="10028-130">If the [FixedSize](fixedsize-control-attribute.md) bit is not set, the loaded image is shrunk or stretched to fit the icon control.</span></span> <span data-ttu-id="10028-131">Если установлен бит [FixedSize](fixedsize-control-attribute.md) , а загруженное изображение меньше, чем элемент управления "значок", изображение отображается в центре элемента управления.</span><span class="sxs-lookup"><span data-stu-id="10028-131">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is smaller than the icon control, the picture is displayed centered inside the control.</span></span> <span data-ttu-id="10028-132">Если установлен бит [FixedSize](fixedsize-control-attribute.md) , а загруженное изображение больше, чем элемент управления "значок", изображение уменьшается в соответствии с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="10028-132">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is larger than the icon control, the picture is reduced to fit the control.</span></span>

<span data-ttu-id="10028-133">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="10028-133">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



