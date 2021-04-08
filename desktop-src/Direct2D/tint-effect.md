---
title: Оттенок
description: Это приведет к оттенок исходного изображения путем умножения исходного изображения на указанный цвет. Он имеет один вход.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988584"
---
# <a name="tint-effect"></a><span data-ttu-id="fe9ec-104">Оттенок</span><span class="sxs-lookup"><span data-stu-id="fe9ec-104">Tint effect</span></span>

<span data-ttu-id="fe9ec-105">Это приведет к оттенок исходного изображения путем умножения исходного изображения на указанный цвет.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-105">This effect tints the source image by multiplying the source image by the specified color.</span></span> <span data-ttu-id="fe9ec-106">Он имеет один вход.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-106">It has a single input.</span></span>

<span data-ttu-id="fe9ec-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1Tint.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-107">The CLSID for this effect is CLSID\_D2D1Tint.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="fe9ec-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="fe9ec-108">Effect properties</span></span>



| <span data-ttu-id="fe9ec-109">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="fe9ec-109">Display name and index enumeration</span></span>                    | <span data-ttu-id="fe9ec-110">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe9ec-110">Type and default value</span></span>                              | <span data-ttu-id="fe9ec-111">Описание</span><span class="sxs-lookup"><span data-stu-id="fe9ec-111">Description</span></span>                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="fe9ec-112">\_Цвет ColorD2D1 оттенка \_ \_ цвета</span><span class="sxs-lookup"><span data-stu-id="fe9ec-112">ColorD2D1\_TINT\_PROP\_COLOR</span></span><br/>               | <span data-ttu-id="fe9ec-113">D2D1 \_ vector \_ 4F (1.0 f, 1.0 f, 1.0 f, 1.0 f)</span><span class="sxs-lookup"><span data-stu-id="fe9ec-113">D2D1\_VECTOR\_4F(1.0f, 1.0f, 1.0f, 1.0f)</span></span><br/> | <span data-ttu-id="fe9ec-114">Цвета из исходного изображения умножаются на это значение.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-114">Colors from the source image are multiplied by this value.</span></span>       |
| <span data-ttu-id="fe9ec-115">\_ \_ \_ Выходные данные среза ClampOutputD2D1 оттенка \_</span><span class="sxs-lookup"><span data-stu-id="fe9ec-115">ClampOutputD2D1\_TINT\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="fe9ec-116">булфалсе</span><span class="sxs-lookup"><span data-stu-id="fe9ec-116">BOOLFALSE</span></span><br/>                                | <span data-ttu-id="fe9ec-117">Указывает, следует ли отменять выходные значения до диапазона \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fe9ec-117">Whether or not to clamp the output values to the range \[0, 1\].</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="fe9ec-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fe9ec-118">Requirements</span></span>



| <span data-ttu-id="fe9ec-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fe9ec-119">Requirement</span></span> | <span data-ttu-id="fe9ec-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fe9ec-120">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="fe9ec-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe9ec-121">Minimum supported client</span></span> | <span data-ttu-id="fe9ec-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="fe9ec-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fe9ec-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe9ec-123">Minimum supported server</span></span> | <span data-ttu-id="fe9ec-124">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="fe9ec-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fe9ec-125">Header</span><span class="sxs-lookup"><span data-stu-id="fe9ec-125">Header</span></span>                   | <span data-ttu-id="fe9ec-126">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="fe9ec-126">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="fe9ec-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe9ec-127">Library</span></span>                  | <span data-ttu-id="fe9ec-128">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="fe9ec-128">d2d1.lib, dxguid.lib</span></span>                              |



 ## <a name="related-topics"></a><span data-ttu-id="fe9ec-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fe9ec-129">Related topics</span></span>

* [<span data-ttu-id="fe9ec-130">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="fe9ec-130">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
