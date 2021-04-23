---
description: Задает уровень энергосбережения видеодекодера.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Свойство Авдеквидеосвповерлевел (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662037"
---
# <a name="avdecvideoswpowerlevel-property"></a><span data-ttu-id="df3a7-103">Авдеквидеосвповерлевел, свойство</span><span class="sxs-lookup"><span data-stu-id="df3a7-103">AVDecVideoSWPowerLevel property</span></span>

<span data-ttu-id="df3a7-104">Задает уровень энергосбережения видеодекодера.</span><span class="sxs-lookup"><span data-stu-id="df3a7-104">Specifies the power-saving level of a video decoder.</span></span>

<span data-ttu-id="df3a7-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="df3a7-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="df3a7-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="df3a7-106">Data type</span></span>

<span data-ttu-id="df3a7-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="df3a7-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="df3a7-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="df3a7-108">Property GUID</span></span>

<span data-ttu-id="df3a7-109">**КОДЕКАПИ \_ авдеквидеосвповерлевел**</span><span class="sxs-lookup"><span data-stu-id="df3a7-109">**CODECAPI\_AVDecVideoSWPowerLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="df3a7-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="df3a7-110">Property value</span></span>

<span data-ttu-id="df3a7-111">Диапазон возможных значений — \[ 0.. 100 \] включительно, со следующим значением.</span><span class="sxs-lookup"><span data-stu-id="df3a7-111">The range of possible values is \[0..100\], inclusive, with the following meaning.</span></span>



| <span data-ttu-id="df3a7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="df3a7-112">Value</span></span> | <span data-ttu-id="df3a7-113">Описание</span><span class="sxs-lookup"><span data-stu-id="df3a7-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="df3a7-114">0</span><span class="sxs-lookup"><span data-stu-id="df3a7-114">0</span></span>     | <span data-ttu-id="df3a7-115">Оптимизировать время работы батареи.</span><span class="sxs-lookup"><span data-stu-id="df3a7-115">Optimize for battery life.</span></span>  |
| <span data-ttu-id="df3a7-116">100</span><span class="sxs-lookup"><span data-stu-id="df3a7-116">100</span></span>   | <span data-ttu-id="df3a7-117">Оптимизировать для качества видео.</span><span class="sxs-lookup"><span data-stu-id="df3a7-117">Optimize for video quality.</span></span> |



 

<span data-ttu-id="df3a7-118">Перечисление [**еавдеквидеосвповерлевел**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) определяет некоторые конкретные константы в этом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="df3a7-118">The [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) enumeration defines some specific constants within this range.</span></span>

## <a name="remarks"></a><span data-ttu-id="df3a7-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df3a7-119">Remarks</span></span>

<span data-ttu-id="df3a7-120">Это свойство можно задать во время воспроизведения, чтобы изменить уровень энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="df3a7-120">You can set this property during playback to change the pwoer-saving level.</span></span>

## <a name="requirements"></a><span data-ttu-id="df3a7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="df3a7-121">Requirements</span></span>



| <span data-ttu-id="df3a7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="df3a7-122">Requirement</span></span> | <span data-ttu-id="df3a7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="df3a7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df3a7-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df3a7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="df3a7-125">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="df3a7-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="df3a7-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df3a7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="df3a7-127">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="df3a7-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="df3a7-128">Header</span><span class="sxs-lookup"><span data-stu-id="df3a7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="df3a7-129"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="df3a7-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df3a7-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df3a7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df3a7-131">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="df3a7-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="df3a7-132">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="df3a7-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




