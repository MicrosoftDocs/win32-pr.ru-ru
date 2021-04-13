---
description: Указывает метод, используемый для кодирования сведений о векторе движения.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: Свойство MFPKEY_DELTAMVRANGEINDEX (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544927"
---
# <a name="mfpkey_deltamvrangeindex-property"></a><span data-ttu-id="24ba3-103">МФПКЭЙ \_ делтамвранжеиндекс, свойство</span><span class="sxs-lookup"><span data-stu-id="24ba3-103">MFPKEY\_DELTAMVRANGEINDEX Property</span></span>

<span data-ttu-id="24ba3-104">Указывает метод, используемый для кодирования сведений о векторе движения.</span><span class="sxs-lookup"><span data-stu-id="24ba3-104">Specifies the method used to encode the motion vector information.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="24ba3-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="24ba3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="24ba3-106">g \_ всзвмвкделтамвранжеиндекс</span><span class="sxs-lookup"><span data-stu-id="24ba3-106">g\_wszWMVCDeltaMVRangeIndex</span></span>

## <a name="data-type"></a><span data-ttu-id="24ba3-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="24ba3-107">Data Type</span></span>

<span data-ttu-id="24ba3-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="24ba3-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="24ba3-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="24ba3-109">Default Value</span></span>

<span data-ttu-id="24ba3-110">0</span><span class="sxs-lookup"><span data-stu-id="24ba3-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="24ba3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24ba3-111">Remarks</span></span>

<span data-ttu-id="24ba3-112">Если это свойство задано, кодировщик увеличивает диапазон разностных векторов движения в полях.</span><span class="sxs-lookup"><span data-stu-id="24ba3-112">If this property is set, the encoder increases the delta motion vector range in fields.</span></span> <span data-ttu-id="24ba3-113">Сведения о векторе движения допустимы только для полей с чередованием.</span><span class="sxs-lookup"><span data-stu-id="24ba3-113">Motion vector information is valid only for interlaced fields.</span></span>

<span data-ttu-id="24ba3-114">Для этого свойства можно задать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="24ba3-114">This property may be set to one of the following values:</span></span>



| <span data-ttu-id="24ba3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="24ba3-115">Value</span></span> | <span data-ttu-id="24ba3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="24ba3-116">Description</span></span>                                                                          |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="24ba3-117">0</span><span class="sxs-lookup"><span data-stu-id="24ba3-117">0</span></span>     | <span data-ttu-id="24ba3-118">Использовать существующий диапазон разностных векторов движения.</span><span class="sxs-lookup"><span data-stu-id="24ba3-118">Use the existing delta motion vector range.</span></span>                                          |
| <span data-ttu-id="24ba3-119">1</span><span class="sxs-lookup"><span data-stu-id="24ba3-119">1</span></span>     | <span data-ttu-id="24ba3-120">Дважды диапазон разностного вектора движения в горизонтальном направлении.</span><span class="sxs-lookup"><span data-stu-id="24ba3-120">Double the delta motion vector range in the horizontal direction.</span></span>                    |
| <span data-ttu-id="24ba3-121">2</span><span class="sxs-lookup"><span data-stu-id="24ba3-121">2</span></span>     | <span data-ttu-id="24ba3-122">Дважды диапазон разностного вектора движения в вертикальном направлении.</span><span class="sxs-lookup"><span data-stu-id="24ba3-122">Double the delta motion vector range in the vertical direction.</span></span>                      |
| <span data-ttu-id="24ba3-123">3</span><span class="sxs-lookup"><span data-stu-id="24ba3-123">3</span></span>     | <span data-ttu-id="24ba3-124">Дважды диапазон разностного вектора движения в горизонтальном и вертикальном направлениях.</span><span class="sxs-lookup"><span data-stu-id="24ba3-124">Double the delta motion vector range in both the horizontal and vertical directions.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="24ba3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="24ba3-125">Requirements</span></span>



| <span data-ttu-id="24ba3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="24ba3-126">Requirement</span></span> | <span data-ttu-id="24ba3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="24ba3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24ba3-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24ba3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="24ba3-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="24ba3-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="24ba3-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24ba3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="24ba3-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24ba3-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24ba3-132">Header</span><span class="sxs-lookup"><span data-stu-id="24ba3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="24ba3-133"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="24ba3-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24ba3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24ba3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ba3-135">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24ba3-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




