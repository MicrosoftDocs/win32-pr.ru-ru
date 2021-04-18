---
title: Воздействие непрозрачности
description: Этот результат корректирует непрозрачность изображения, умножая альфа-канал входных данных на заданное значение прозрачности. Он имеет один вход.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681998"
---
# <a name="opacity-effect"></a><span data-ttu-id="004de-104">Воздействие непрозрачности</span><span class="sxs-lookup"><span data-stu-id="004de-104">Opacity effect</span></span>

<span data-ttu-id="004de-105">Этот результат корректирует непрозрачность изображения, умножая альфа-канал входных данных на заданное значение прозрачности.</span><span class="sxs-lookup"><span data-stu-id="004de-105">This effect adjusts the opacity of an image by multiplying the alpha channel of the input by the specified opacity value.</span></span> <span data-ttu-id="004de-106">Он имеет один вход.</span><span class="sxs-lookup"><span data-stu-id="004de-106">It has a single input.</span></span>

<span data-ttu-id="004de-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1Opacity.</span><span class="sxs-lookup"><span data-stu-id="004de-107">The CLSID for this effect is CLSID\_D2D1Opacity.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="004de-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="004de-108">Effect properties</span></span>



| <span data-ttu-id="004de-109">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="004de-109">Display name and index enumeration</span></span>              | <span data-ttu-id="004de-110">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="004de-110">Type and default value</span></span> | <span data-ttu-id="004de-111">Описание</span><span class="sxs-lookup"><span data-stu-id="004de-111">Description</span></span>                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="004de-112">Непрозрачность свойства непрозрачности \_ D2D1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="004de-112">Opacity D2D1\_OPACITY\_PROP\_OPACITY</span></span><br/> | <span data-ttu-id="004de-113">FLOAT 1.0 f</span><span class="sxs-lookup"><span data-stu-id="004de-113">FLOAT1.0f</span></span><br/>   | <span data-ttu-id="004de-114">Множитель для альфа-канала входного изображения.</span><span class="sxs-lookup"><span data-stu-id="004de-114">The multiplier to the input image's alpha channel.</span></span> <span data-ttu-id="004de-115">Минимальное значение — 0,0 f, а максимальное значение — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="004de-115">The minimum value is 0.0f and the maximum value is 1.0f.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="004de-116">Требования</span><span class="sxs-lookup"><span data-stu-id="004de-116">Requirements</span></span>



| <span data-ttu-id="004de-117">Требование</span><span class="sxs-lookup"><span data-stu-id="004de-117">Requirement</span></span> | <span data-ttu-id="004de-118">Значение</span><span class="sxs-lookup"><span data-stu-id="004de-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="004de-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="004de-119">Minimum supported client</span></span> | <span data-ttu-id="004de-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="004de-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="004de-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="004de-121">Minimum supported server</span></span> | <span data-ttu-id="004de-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="004de-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="004de-123">Header</span><span class="sxs-lookup"><span data-stu-id="004de-123">Header</span></span>                   | <span data-ttu-id="004de-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="004de-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="004de-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="004de-125">Library</span></span>                  | <span data-ttu-id="004de-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="004de-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="004de-127">См. также</span><span class="sxs-lookup"><span data-stu-id="004de-127">Related topics</span></span>

* [<span data-ttu-id="004de-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="004de-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
