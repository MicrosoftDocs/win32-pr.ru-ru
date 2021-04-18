---
description: Задает конечный уровень буфера кодирования (в битах) в конце процесса кодирования. Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Свойство Авенккоммонбуффераутлевел (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662046"
---
# <a name="avenccommonbufferoutlevel-property"></a><span data-ttu-id="54cf8-104">Авенккоммонбуффераутлевел, свойство</span><span class="sxs-lookup"><span data-stu-id="54cf8-104">AVEncCommonBufferOutLevel property</span></span>

<span data-ttu-id="54cf8-105">Задает конечный уровень буфера кодирования (в битах) в конце процесса кодирования.</span><span class="sxs-lookup"><span data-stu-id="54cf8-105">Specifies the final level of the encoding buffer, in bits, at the end of the encoding process.</span></span> <span data-ttu-id="54cf8-106">Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).</span><span class="sxs-lookup"><span data-stu-id="54cf8-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="54cf8-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="54cf8-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="54cf8-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="54cf8-108">Data type</span></span>

<span data-ttu-id="54cf8-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="54cf8-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="54cf8-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="54cf8-110">Property GUID</span></span>

<span data-ttu-id="54cf8-111">**КОДЕКАПИ \_ авенккоммонбуффераутлевел**</span><span class="sxs-lookup"><span data-stu-id="54cf8-111">**CODECAPI\_AVEncCommonBufferOutLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="54cf8-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="54cf8-112">Property value</span></span>

<span data-ttu-id="54cf8-113">Это свойство имеет линейный Диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="54cf8-113">This property has a linear range of values.</span></span> <span data-ttu-id="54cf8-114">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="54cf8-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="54cf8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54cf8-115">Remarks</span></span>

<span data-ttu-id="54cf8-116">Свойство доступно только в том случае, если длительность кодирования определена заранее с помощью свойства [**авенквидеонуффиелдстоенкоде**](avencvideonooffieldstoencode-property.md) или свойства [**авенкаудиоинтервалтоенкоде**](avencaudiointervaltoencode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="54cf8-116">The property is available only if the encoding duration is defined in advance, using the [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) property or [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) property.</span></span>

<span data-ttu-id="54cf8-117">Для видео в формате MPEG это свойство определяет заполнение видеобуфера (ВБВ) в конце процесса кодирования.</span><span class="sxs-lookup"><span data-stu-id="54cf8-117">For MPEG video, this property defines the video buffer verifier (VBV) fullness at the end of the encoding process.</span></span> <span data-ttu-id="54cf8-118">Он поддерживает объединение потоков во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="54cf8-118">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="54cf8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="54cf8-119">Requirements</span></span>



| <span data-ttu-id="54cf8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="54cf8-120">Requirement</span></span> | <span data-ttu-id="54cf8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="54cf8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54cf8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54cf8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54cf8-123">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="54cf8-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="54cf8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54cf8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54cf8-125">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="54cf8-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="54cf8-126">Header</span><span class="sxs-lookup"><span data-stu-id="54cf8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54cf8-127"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="54cf8-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54cf8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54cf8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54cf8-129">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="54cf8-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="54cf8-130">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="54cf8-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




