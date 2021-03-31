---
description: Указывает, создает ли кодировщик открытые группы изображений (группы GOP) или закрытый группы GOP. Это свойство применяется к кодировщикам видео MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Свойство Авенкмпвгопопен (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806346"
---
# <a name="avencmpvgopopen-property"></a><span data-ttu-id="4c576-104">Авенкмпвгопопен, свойство</span><span class="sxs-lookup"><span data-stu-id="4c576-104">AVEncMPVGOPOpen property</span></span>

<span data-ttu-id="4c576-105">Указывает, создает ли кодировщик открытые группы изображений (группы GOP) или закрытый группы GOP.</span><span class="sxs-lookup"><span data-stu-id="4c576-105">Specifies whether the encoder produces open groups of pictures (GOPs) or closed GOPs.</span></span> <span data-ttu-id="4c576-106">Это свойство применяется к кодировщикам видео MPEG.</span><span class="sxs-lookup"><span data-stu-id="4c576-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="4c576-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4c576-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4c576-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4c576-108">Data type</span></span>

<span data-ttu-id="4c576-109">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="4c576-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4c576-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="4c576-110">Property GUID</span></span>

<span data-ttu-id="4c576-111">**КОДЕКАПИ \_ авенкмпвгопопен**</span><span class="sxs-lookup"><span data-stu-id="4c576-111">**CODECAPI\_AVEncMPVGOPOpen**</span></span>

## <a name="property-value"></a><span data-ttu-id="4c576-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4c576-112">Property value</span></span>



| <span data-ttu-id="4c576-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4c576-113">Value</span></span>          | <span data-ttu-id="4c576-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4c576-114">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="4c576-115">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="4c576-115">VARIANT\_FALSE</span></span> | <span data-ttu-id="4c576-116">Закрытые группы GOP</span><span class="sxs-lookup"><span data-stu-id="4c576-116">Closed GOPs</span></span> |
| <span data-ttu-id="4c576-117">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="4c576-117">VARIANT\_TRUE</span></span>  | <span data-ttu-id="4c576-118">Открыть группы GOP</span><span class="sxs-lookup"><span data-stu-id="4c576-118">Open GOPs</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="4c576-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c576-119">Remarks</span></span>

<span data-ttu-id="4c576-120">Открытый GOP содержит разностные кадры, которые ссылаются на кадры из предыдущего GOP.</span><span class="sxs-lookup"><span data-stu-id="4c576-120">An open GOP contains delta frames that reference frames from the previous GOP.</span></span> <span data-ttu-id="4c576-121">Закрытый GOP не содержит никаких разностных кадров, ссылающихся на предыдущий GOP.</span><span class="sxs-lookup"><span data-stu-id="4c576-121">A closed GOP does not contain any delta frames that reference the previous GOP.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c576-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4c576-122">Requirements</span></span>



| <span data-ttu-id="4c576-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4c576-123">Requirement</span></span> | <span data-ttu-id="4c576-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4c576-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c576-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c576-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4c576-126">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4c576-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4c576-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c576-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4c576-128">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="4c576-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4c576-129">Header</span><span class="sxs-lookup"><span data-stu-id="4c576-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c576-130"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c576-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c576-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c576-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c576-132">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="4c576-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4c576-133">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="4c576-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




