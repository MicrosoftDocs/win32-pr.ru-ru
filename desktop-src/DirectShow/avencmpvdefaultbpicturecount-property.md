---
description: Указывает число последовательных кадров B между кадрами I и P по умолчанию.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Свойство Авенкмпвдефаултбпиктурекаунт (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072285"
---
# <a name="avencmpvdefaultbpicturecount-property"></a><span data-ttu-id="b55e2-103">Авенкмпвдефаултбпиктурекаунт, свойство</span><span class="sxs-lookup"><span data-stu-id="b55e2-103">AVEncMPVDefaultBPictureCount property</span></span>

<span data-ttu-id="b55e2-104">Указывает число последовательных кадров B между кадрами I и P по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b55e2-104">Specifies the default number of consecutive B frames between I and P frames.</span></span>

<span data-ttu-id="b55e2-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b55e2-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b55e2-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b55e2-106">Data type</span></span>

<span data-ttu-id="b55e2-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b55e2-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b55e2-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="b55e2-108">Property GUID</span></span>

<span data-ttu-id="b55e2-109">**КОДЕКАПИ \_ авенкмпвдефаултбпиктурекаунт**</span><span class="sxs-lookup"><span data-stu-id="b55e2-109">**CODECAPI\_AVEncMPVDefaultBPictureCount**</span></span>

## <a name="property-value"></a><span data-ttu-id="b55e2-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b55e2-110">Property value</span></span>

<span data-ttu-id="b55e2-111">Это свойство имеет линейный Диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="b55e2-111">This property has a linear range of values.</span></span> <span data-ttu-id="b55e2-112">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="b55e2-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="b55e2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b55e2-113">Remarks</span></span>

<span data-ttu-id="b55e2-114">До Windows 8 это свойство применяется к кодировщикам видео MPEG.</span><span class="sxs-lookup"><span data-stu-id="b55e2-114">Prior to Windows 8, this property applies to MPEG video encoders.</span></span> <span data-ttu-id="b55e2-115">Начиная с Windows 8, это свойство используется кодировщиками видео MPEG, WMV и H. 264.</span><span class="sxs-lookup"><span data-stu-id="b55e2-115">Starting with Windows 8, this property is used by MPEG, WMV, and H.264 video encoders.</span></span>

<span data-ttu-id="b55e2-116">Если кодировщик поддерживает это свойство, его можно использовать для управления структурой групп рисунков (GOP).</span><span class="sxs-lookup"><span data-stu-id="b55e2-116">If the encoder supports this property, it can be used to control the group of pictures (GOP) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b55e2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b55e2-117">Requirements</span></span>



| <span data-ttu-id="b55e2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b55e2-118">Requirement</span></span> | <span data-ttu-id="b55e2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b55e2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b55e2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b55e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b55e2-121">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b55e2-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b55e2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b55e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b55e2-123">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="b55e2-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b55e2-124">Header</span><span class="sxs-lookup"><span data-stu-id="b55e2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b55e2-125"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b55e2-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b55e2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b55e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b55e2-127">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="b55e2-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b55e2-128">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="b55e2-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




