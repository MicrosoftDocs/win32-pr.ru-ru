---
description: Указывает максимальное количество рисунков из одного заголовка Group-of-Pictures (GOP) в следующий заголовок GOP.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Свойство Авенкмпвгопсизе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072282"
---
# <a name="avencmpvgopsize-property"></a><span data-ttu-id="8c0d5-103">Авенкмпвгопсизе, свойство</span><span class="sxs-lookup"><span data-stu-id="8c0d5-103">AVEncMPVGOPSize property</span></span>

<span data-ttu-id="8c0d5-104">Указывает максимальное количество рисунков из одного заголовка Group-of-Pictures (GOP) в следующий заголовок GOP.</span><span class="sxs-lookup"><span data-stu-id="8c0d5-104">Specifies the maximum number of pictures from one group-of-pictures (GOP) header to the next GOP header.</span></span>

<span data-ttu-id="8c0d5-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8c0d5-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8c0d5-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8c0d5-106">Data type</span></span>

<span data-ttu-id="8c0d5-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8c0d5-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8c0d5-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="8c0d5-108">Property GUID</span></span>

<span data-ttu-id="8c0d5-109">**КОДЕКАПИ \_ авенкмпвгопсизе**</span><span class="sxs-lookup"><span data-stu-id="8c0d5-109">**CODECAPI\_AVEncMPVGOPSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="8c0d5-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8c0d5-110">Property value</span></span>

<span data-ttu-id="8c0d5-111">Кодировщики могут реализовывать это свойство как перечислимый набор или как линейный Диапазон.</span><span class="sxs-lookup"><span data-stu-id="8c0d5-111">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c0d5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c0d5-112">Remarks</span></span>

<span data-ttu-id="8c0d5-113">Задайте это свойство перед началом записи.</span><span class="sxs-lookup"><span data-stu-id="8c0d5-113">Set this property before starting a recording.</span></span>

<span data-ttu-id="8c0d5-114">**Применимо к Windows 8:** Закодированный GOP размер должен быть меньше или равен указанному числу через это свойство, чтобы тот же самый шаблон кадра B, установленный [кодекапи \_ авенкмпвдефаултбпиктурекаунт](avencmpvdefaultbpicturecount-property.md) на протяжении GOP или из-за изменения сцены.</span><span class="sxs-lookup"><span data-stu-id="8c0d5-114">**Applies to Windows 8:** The encoded GOP size shall be smaller than or equal to the specified number through this property, in order to keep the same B frame pattern set by [CODECAPI\_AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) throughout the GOP or due to scene change.</span></span> <span data-ttu-id="8c0d5-115">Например, если число кадров B в GOP задано равным 2, а размер GOP — 11, кодировщик должен создать GOP размер 10 кадров или меньше.</span><span class="sxs-lookup"><span data-stu-id="8c0d5-115">For example, when the number of B frames in a GOP is specified to be 2, and GOP size is 11, then encoder shall produce GOP size of 10 frames or less.</span></span> <span data-ttu-id="8c0d5-116">Когда изменение сцены происходит в середине GOP, кодировщик может также вставить ключевой кадр и создать меньший GOP.</span><span class="sxs-lookup"><span data-stu-id="8c0d5-116">When scene change happens in the middle of a GOP, encoder might also insert key frame and produce smaller GOP.</span></span>

<span data-ttu-id="8c0d5-117">Размер GOP 0 зависит от кодировщика. Кодировщики могут выбирать различные размеры GOP в зависимости от их реализации, качества и производительности.</span><span class="sxs-lookup"><span data-stu-id="8c0d5-117">GOP size 0 is encoder dependent and encoders can choose different GOP sizes based on their implementation/quality/performance.</span></span> <span data-ttu-id="8c0d5-118">В этом случае кодировщики должны учитывать в этом случае кадры GOP size и Truncate B.</span><span class="sxs-lookup"><span data-stu-id="8c0d5-118">Encoders should honor the GOP size and truncate B frames in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0d5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8c0d5-119">Requirements</span></span>



| <span data-ttu-id="8c0d5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8c0d5-120">Requirement</span></span> | <span data-ttu-id="8c0d5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8c0d5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0d5-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c0d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0d5-123">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8c0d5-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8c0d5-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c0d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0d5-125">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="8c0d5-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8c0d5-126">Header</span><span class="sxs-lookup"><span data-stu-id="8c0d5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c0d5-127"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c0d5-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c0d5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c0d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0d5-129">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="8c0d5-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8c0d5-130">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="8c0d5-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




