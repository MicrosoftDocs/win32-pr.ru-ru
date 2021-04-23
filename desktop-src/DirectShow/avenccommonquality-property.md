---
description: Задает уровень качества кодирования.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Свойство Авенккоммонкуалити (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495636"
---
# <a name="avenccommonquality-property"></a><span data-ttu-id="ce5f2-103">Авенккоммонкуалити, свойство</span><span class="sxs-lookup"><span data-stu-id="ce5f2-103">AVEncCommonQuality property</span></span>

<span data-ttu-id="ce5f2-104">Задает уровень качества кодирования.</span><span class="sxs-lookup"><span data-stu-id="ce5f2-104">Specifies the quality level for encoding.</span></span>

<span data-ttu-id="ce5f2-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ce5f2-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ce5f2-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ce5f2-106">Data type</span></span>

<span data-ttu-id="ce5f2-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="ce5f2-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ce5f2-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="ce5f2-108">Property GUID</span></span>

<span data-ttu-id="ce5f2-109">**КОДЕКАПИ \_ авенккоммонкуалити**</span><span class="sxs-lookup"><span data-stu-id="ce5f2-109">**CODECAPI\_AVEncCommonQuality**</span></span>

## <a name="property-value"></a><span data-ttu-id="ce5f2-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ce5f2-110">Property value</span></span>

<span data-ttu-id="ce5f2-111">Значение этого свойства имеет следующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="ce5f2-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="ce5f2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="ce5f2-112">Value</span></span> | <span data-ttu-id="ce5f2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ce5f2-113">Description</span></span>                           |
|-------|---------------------------------------|
| <span data-ttu-id="ce5f2-114">0</span><span class="sxs-lookup"><span data-stu-id="ce5f2-114">0</span></span>     | <span data-ttu-id="ce5f2-115">Минимальное качество, меньший размер выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ce5f2-115">Minimum quality, smaller output size.</span></span> |
| <span data-ttu-id="ce5f2-116">100</span><span class="sxs-lookup"><span data-stu-id="ce5f2-116">100</span></span>   | <span data-ttu-id="ce5f2-117">Максимальное качество, больший размер вывода.</span><span class="sxs-lookup"><span data-stu-id="ce5f2-117">Maximum quality, larger output size.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="ce5f2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce5f2-118">Remarks</span></span>

<span data-ttu-id="ce5f2-119">Это свойство управляет уровнем качества, если кодировщик не использует ограничение скорости.</span><span class="sxs-lookup"><span data-stu-id="ce5f2-119">This property controls the quality level when the encoder is not using a constrained bit rate.</span></span> <span data-ttu-id="ce5f2-120">Свойство [**авенккоммонратеконтролмоде**](avenccommonratecontrolmode-property.md) определяет, ограничена ли скорость потока.</span><span class="sxs-lookup"><span data-stu-id="ce5f2-120">The [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) property determines whether the bit rate is constrained.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce5f2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ce5f2-121">Requirements</span></span>



| <span data-ttu-id="ce5f2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ce5f2-122">Requirement</span></span> | <span data-ttu-id="ce5f2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ce5f2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5f2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce5f2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ce5f2-125">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ce5f2-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ce5f2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce5f2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ce5f2-127">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="ce5f2-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ce5f2-128">Header</span><span class="sxs-lookup"><span data-stu-id="ce5f2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce5f2-129"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce5f2-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce5f2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce5f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5f2-131">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="ce5f2-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ce5f2-132">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="ce5f2-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




