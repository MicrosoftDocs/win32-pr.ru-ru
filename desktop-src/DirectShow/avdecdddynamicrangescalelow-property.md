---
description: Указывает низкоуровневые улучшения, когда декодер выполняет динамическое управление диапазонами в аудио потоке Dolby AC-3.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Свойство Авдекдддинамикранжескалелов (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b68b1d4376d9ba15859be943ded23458fe16d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072306"
---
# <a name="avdecdddynamicrangescalelow-property"></a><span data-ttu-id="42d88-103">Авдекдддинамикранжескалелов, свойство</span><span class="sxs-lookup"><span data-stu-id="42d88-103">AVDecDDDynamicRangeScaleLow property</span></span>

<span data-ttu-id="42d88-104">Указывает низкоуровневые улучшения, когда декодер выполняет динамическое управление диапазонами в аудио потоке Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="42d88-104">Specifies the low-level boost when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="42d88-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="42d88-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="42d88-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="42d88-106">Data type</span></span>

<span data-ttu-id="42d88-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="42d88-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="42d88-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="42d88-108">Property GUID</span></span>

<span data-ttu-id="42d88-109">**КОДЕКАПИ \_ авдекдддинамикранжескалелов**</span><span class="sxs-lookup"><span data-stu-id="42d88-109">**CODECAPI\_AVDecDDDynamicRangeScaleLow**</span></span>

## <a name="property-value"></a><span data-ttu-id="42d88-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="42d88-110">Property value</span></span>

<span data-ttu-id="42d88-111">Значение этого свойства имеет следующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="42d88-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="42d88-112">Значение</span><span class="sxs-lookup"><span data-stu-id="42d88-112">Value</span></span> | <span data-ttu-id="42d88-113">Описание</span><span class="sxs-lookup"><span data-stu-id="42d88-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="42d88-114">0</span><span class="sxs-lookup"><span data-stu-id="42d88-114">0</span></span>     | <span data-ttu-id="42d88-115">Отсутствует динамическое сжатие диапазона.</span><span class="sxs-lookup"><span data-stu-id="42d88-115">No dynamic range compression.</span></span> <span data-ttu-id="42d88-116">Сохраните полный динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="42d88-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="42d88-117">100</span><span class="sxs-lookup"><span data-stu-id="42d88-117">100</span></span>   | <span data-ttu-id="42d88-118">Применить полное сжатие динамического диапазона.</span><span class="sxs-lookup"><span data-stu-id="42d88-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="42d88-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42d88-119">Remarks</span></span>

<span data-ttu-id="42d88-120">Это свойство применяется только в том случае, если свойство [**авдекддоператионалмоде**](avdecddoperationalmode-property.md) имеет значение еавдекддоператионалмоде \_ line.</span><span class="sxs-lookup"><span data-stu-id="42d88-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d88-121">Требования</span><span class="sxs-lookup"><span data-stu-id="42d88-121">Requirements</span></span>



| <span data-ttu-id="42d88-122">Требование</span><span class="sxs-lookup"><span data-stu-id="42d88-122">Requirement</span></span> | <span data-ttu-id="42d88-123">Значение</span><span class="sxs-lookup"><span data-stu-id="42d88-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42d88-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42d88-124">Minimum supported client</span></span><br/> | <span data-ttu-id="42d88-125">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="42d88-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="42d88-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42d88-126">Minimum supported server</span></span><br/> | <span data-ttu-id="42d88-127">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="42d88-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="42d88-128">Header</span><span class="sxs-lookup"><span data-stu-id="42d88-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="42d88-129"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d88-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42d88-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42d88-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d88-131">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="42d88-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="42d88-132">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="42d88-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




