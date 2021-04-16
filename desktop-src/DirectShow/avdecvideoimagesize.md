---
description: Возвращает размер декодированного изображения в пикселях.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Свойство Авдеквидеоимажесизе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662049"
---
# <a name="avdecvideoimagesize-property"></a><span data-ttu-id="8d4c1-103">Авдеквидеоимажесизе, свойство</span><span class="sxs-lookup"><span data-stu-id="8d4c1-103">AVDecVideoImageSize property</span></span>

<span data-ttu-id="8d4c1-104">Возвращает размер декодированного изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-104">Gets the size of the decoded image, in pixels.</span></span>

<span data-ttu-id="8d4c1-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="8d4c1-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8d4c1-106">Data type</span></span>

<span data-ttu-id="8d4c1-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8d4c1-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8d4c1-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="8d4c1-108">Property GUID</span></span>

<span data-ttu-id="8d4c1-109">**КОДЕКАПИ \_ авдеквидеоимажесизе**</span><span class="sxs-lookup"><span data-stu-id="8d4c1-109">**CODECAPI\_AVDecVideoImageSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="8d4c1-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8d4c1-110">Property value</span></span>

<span data-ttu-id="8d4c1-111">Старшие 16 бит содержат ширину, а младшие 16 бит содержат высоту.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-111">The high 16 bits contain the width, and the low 16 bits contain the height.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d4c1-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d4c1-112">Remarks</span></span>

<span data-ttu-id="8d4c1-113">Число каналов включает канал с низкой частотой (НИЗКОЧАСТОТный), если он присутствует.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d4c1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8d4c1-114">Requirements</span></span>



| <span data-ttu-id="8d4c1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8d4c1-115">Requirement</span></span> | <span data-ttu-id="8d4c1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8d4c1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d4c1-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d4c1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8d4c1-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8d4c1-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8d4c1-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d4c1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8d4c1-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="8d4c1-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8d4c1-121">Header</span><span class="sxs-lookup"><span data-stu-id="8d4c1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d4c1-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d4c1-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d4c1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d4c1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d4c1-124">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="8d4c1-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8d4c1-125">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="8d4c1-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




