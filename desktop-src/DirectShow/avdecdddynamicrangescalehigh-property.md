---
description: Задает высокоуровневая вырезание, когда декодер выполняет динамическое управление диапазонами в потоке звука Dolby AC-3.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Свойство Авдекдддинамикранжескалехигх (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495462"
---
# <a name="avdecdddynamicrangescalehigh-property"></a><span data-ttu-id="a3e22-103">Авдекдддинамикранжескалехигх, свойство</span><span class="sxs-lookup"><span data-stu-id="a3e22-103">AVDecDDDynamicRangeScaleHigh property</span></span>

<span data-ttu-id="a3e22-104">Задает высокоуровневая вырезание, когда декодер выполняет динамическое управление диапазонами в потоке звука Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="a3e22-104">Specifies the high-level cut when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="a3e22-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a3e22-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a3e22-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a3e22-106">Data type</span></span>

<span data-ttu-id="a3e22-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a3e22-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a3e22-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="a3e22-108">Property GUID</span></span>

<span data-ttu-id="a3e22-109">**КОДЕКАПИ \_ авдекдддинамикранжескалехигх**</span><span class="sxs-lookup"><span data-stu-id="a3e22-109">**CODECAPI\_AVDecDDDynamicRangeScaleHigh**</span></span>

## <a name="property-value"></a><span data-ttu-id="a3e22-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a3e22-110">Property value</span></span>

<span data-ttu-id="a3e22-111">Значение этого свойства имеет следующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="a3e22-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="a3e22-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a3e22-112">Value</span></span> | <span data-ttu-id="a3e22-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e22-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="a3e22-114">0</span><span class="sxs-lookup"><span data-stu-id="a3e22-114">0</span></span>     | <span data-ttu-id="a3e22-115">Отсутствует динамическое сжатие диапазона.</span><span class="sxs-lookup"><span data-stu-id="a3e22-115">No dynamic range compression.</span></span> <span data-ttu-id="a3e22-116">Сохраните полный динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="a3e22-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="a3e22-117">100</span><span class="sxs-lookup"><span data-stu-id="a3e22-117">100</span></span>   | <span data-ttu-id="a3e22-118">Применить полное сжатие динамического диапазона.</span><span class="sxs-lookup"><span data-stu-id="a3e22-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="a3e22-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3e22-119">Remarks</span></span>

<span data-ttu-id="a3e22-120">Это свойство применяется только в том случае, если свойство [**авдекддоператионалмоде**](avdecddoperationalmode-property.md) имеет значение еавдекддоператионалмоде \_ line.</span><span class="sxs-lookup"><span data-stu-id="a3e22-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e22-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a3e22-121">Requirements</span></span>



| <span data-ttu-id="a3e22-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a3e22-122">Requirement</span></span> | <span data-ttu-id="a3e22-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a3e22-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e22-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3e22-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e22-125">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a3e22-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a3e22-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3e22-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e22-127">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="a3e22-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a3e22-128">Header</span><span class="sxs-lookup"><span data-stu-id="a3e22-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3e22-129"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3e22-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3e22-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3e22-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e22-131">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="a3e22-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a3e22-132">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="a3e22-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




