---
description: Включает или отключает аппаратное ускорение для декодирования видео VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: Свойство AVDecVideoAcceleration_VC1 (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655603"
---
# <a name="avdecvideoacceleration_vc1-property"></a><span data-ttu-id="4e163-103">Авдеквидеоакцелератион \_ VC1, свойство</span><span class="sxs-lookup"><span data-stu-id="4e163-103">AVDecVideoAcceleration\_VC1 property</span></span>

<span data-ttu-id="4e163-104">Включает или отключает аппаратное ускорение для декодирования видео VC-1.</span><span class="sxs-lookup"><span data-stu-id="4e163-104">Enables or disables hardware acceleration for VC-1 video decoding.</span></span>

<span data-ttu-id="4e163-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4e163-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4e163-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4e163-106">Data type</span></span>

<span data-ttu-id="4e163-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="4e163-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4e163-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="4e163-108">Property GUID</span></span>

<span data-ttu-id="4e163-109">**КОДЕКАПИ \_ авдеквидеоакцелератион \_ VC1**</span><span class="sxs-lookup"><span data-stu-id="4e163-109">**CODECAPI\_AVDecVideoAcceleration\_VC1**</span></span>

## <a name="remarks"></a><span data-ttu-id="4e163-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e163-110">Remarks</span></span>

<span data-ttu-id="4e163-111">Если значение равно нулю, декодер не использует ускорение видео DirectX (ДКСВА) для декодирования видео VC-1.</span><span class="sxs-lookup"><span data-stu-id="4e163-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for VC-1 video decoding.</span></span> <span data-ttu-id="4e163-112">Для фильтров DirectShow установите это свойство перед подключением выходного ПИН-кода декодера.</span><span class="sxs-lookup"><span data-stu-id="4e163-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e163-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4e163-113">Requirements</span></span>



| <span data-ttu-id="4e163-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4e163-114">Requirement</span></span> | <span data-ttu-id="4e163-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4e163-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e163-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e163-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4e163-117">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e163-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4e163-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e163-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4e163-119">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="4e163-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4e163-120">Header</span><span class="sxs-lookup"><span data-stu-id="4e163-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e163-121"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e163-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e163-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e163-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e163-123">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="4e163-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4e163-124">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="4e163-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




