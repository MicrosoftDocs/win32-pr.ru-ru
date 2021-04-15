---
description: Задает уровень смешения в децибел (dB) в потоке цифрового звука Dolby. Это свойство применяется к кодировщикам цифрового аудио Dolby.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Свойство Авенкддпродуктионмикслевел (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662041"
---
# <a name="avencddproductionmixlevel-property"></a><span data-ttu-id="e68f6-104">Авенкддпродуктионмикслевел, свойство</span><span class="sxs-lookup"><span data-stu-id="e68f6-104">AVEncDDProductionMixLevel property</span></span>

<span data-ttu-id="e68f6-105">Задает уровень смешения в децибел (dB) в потоке цифрового звука Dolby.</span><span class="sxs-lookup"><span data-stu-id="e68f6-105">Specifies the mixing level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="e68f6-106">Это свойство применяется к кодировщикам цифрового аудио Dolby.</span><span class="sxs-lookup"><span data-stu-id="e68f6-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="e68f6-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e68f6-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="e68f6-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e68f6-108">Data type</span></span>

<span data-ttu-id="e68f6-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="e68f6-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e68f6-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="e68f6-110">Property GUID</span></span>

<span data-ttu-id="e68f6-111">**КОДЕКАПИ \_ авенкддпродуктионмикслевел**</span><span class="sxs-lookup"><span data-stu-id="e68f6-111">**CODECAPI\_AVEncDDProductionMixLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="e68f6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e68f6-112">Property value</span></span>

<span data-ttu-id="e68f6-113">Это свойство имеет линейный Диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="e68f6-113">This property has a linear range of values.</span></span> <span data-ttu-id="e68f6-114">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="e68f6-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="e68f6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e68f6-115">Remarks</span></span>

<span data-ttu-id="e68f6-116">Если это свойство задано, задайте для свойства [**авенкддпродуктионинфоексистс**](avencddproductioninfoexists-property.md) значение **true**.</span><span class="sxs-lookup"><span data-stu-id="e68f6-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e68f6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e68f6-117">Requirements</span></span>



| <span data-ttu-id="e68f6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e68f6-118">Requirement</span></span> | <span data-ttu-id="e68f6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e68f6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e68f6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e68f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e68f6-121">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e68f6-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e68f6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e68f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e68f6-123">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="e68f6-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e68f6-124">Header</span><span class="sxs-lookup"><span data-stu-id="e68f6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e68f6-125"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="e68f6-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e68f6-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e68f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68f6-127">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="e68f6-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="e68f6-128">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="e68f6-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




