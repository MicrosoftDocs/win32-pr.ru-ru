---
description: Результат установки альфа-канала
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Результат установки альфа-канала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805927"
---
# <a name="alpha-setter-effect"></a><span data-ttu-id="4cb5a-103">Результат установки альфа-канала</span><span class="sxs-lookup"><span data-stu-id="4cb5a-103">Alpha Setter Effect</span></span>

> [!Note]  
> <span data-ttu-id="4cb5a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4cb5a-104">\[Deprecated.</span></span> <span data-ttu-id="4cb5a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4cb5a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4cb5a-106">Этот параметр задает альфа-биты на видеоизображении.</span><span class="sxs-lookup"><span data-stu-id="4cb5a-106">The Alpha Setter effect sets the alpha bits on a video image.</span></span>

<span data-ttu-id="4cb5a-107">Идентификатор класса (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span><span class="sxs-lookup"><span data-stu-id="4cb5a-107">Class ID (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span></span>

<span data-ttu-id="4cb5a-108">Имя переменной CLSID: CLSID \_ дксталфасеттер</span><span class="sxs-lookup"><span data-stu-id="4cb5a-108">CLSID Variable Name: CLSID\_DxtAlphaSetter</span></span>

<span data-ttu-id="4cb5a-109">Понятное имя: "Дксталфасеттер"</span><span class="sxs-lookup"><span data-stu-id="4cb5a-109">Friendly Name: "DxtAlphaSetter"</span></span>

### <a name="properties"></a><span data-ttu-id="4cb5a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4cb5a-110">Properties</span></span>



| <span data-ttu-id="4cb5a-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="4cb5a-111">Property</span></span>  | <span data-ttu-id="4cb5a-112">Тип</span><span class="sxs-lookup"><span data-stu-id="4cb5a-112">Type</span></span>   | <span data-ttu-id="4cb5a-113">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="4cb5a-113">Default</span></span> | <span data-ttu-id="4cb5a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4cb5a-114">Description</span></span>                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| <span data-ttu-id="4cb5a-115">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="4cb5a-115">Alpha</span></span>     | <span data-ttu-id="4cb5a-116">BYTE</span><span class="sxs-lookup"><span data-stu-id="4cb5a-116">BYTE</span></span>   | <span data-ttu-id="4cb5a-117">-1</span><span class="sxs-lookup"><span data-stu-id="4cb5a-117">-1</span></span>      | <span data-ttu-id="4cb5a-118">Задает альфа-канал для всего изображения.</span><span class="sxs-lookup"><span data-stu-id="4cb5a-118">Sets the alpha for the entire image.</span></span>                        |
| <span data-ttu-id="4cb5a-119">алфарамп</span><span class="sxs-lookup"><span data-stu-id="4cb5a-119">AlphaRamp</span></span> | <span data-ttu-id="4cb5a-120">double</span><span class="sxs-lookup"><span data-stu-id="4cb5a-120">double</span></span> | <span data-ttu-id="4cb5a-121">-1.0</span><span class="sxs-lookup"><span data-stu-id="4cb5a-121">-1.0</span></span>    | <span data-ttu-id="4cb5a-122">Задает значение альфа в процентах от исходного альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="4cb5a-122">Sets the alpha as a percentage of the original alpha value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4cb5a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cb5a-123">Remarks</span></span>

<span data-ttu-id="4cb5a-124">Свойство с отрицательным значением игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4cb5a-124">A property with a negative value is ignored.</span></span> <span data-ttu-id="4cb5a-125">Только одно свойство может иметь неотрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="4cb5a-125">Only one property can have a non-negative value.</span></span> <span data-ttu-id="4cb5a-126">Свойство alpha задает константное альфа-значение для каждого пикселя в изображении.</span><span class="sxs-lookup"><span data-stu-id="4cb5a-126">The Alpha property specifies a constant alpha value for every pixel in the image.</span></span> <span data-ttu-id="4cb5a-127">Это свойство перезаписывает альфа-значения из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="4cb5a-127">This property overwrites the alpha values from the original image.</span></span> <span data-ttu-id="4cb5a-128">Свойство Алфарамп задает альфа-значение каждого пикселя в процентах от исходного значения пикселя от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="4cb5a-128">The AlphaRamp property specifies each pixel's alpha value as a percentage of the pixel's original value, from 0.0 to 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cb5a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4cb5a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cb5a-130">Альфа-смешение</span><span class="sxs-lookup"><span data-stu-id="4cb5a-130">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



