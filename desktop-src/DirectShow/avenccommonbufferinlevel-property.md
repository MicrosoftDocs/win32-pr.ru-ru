---
description: Задает начальный уровень буфера кодирования в битах. Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Свойство Авенккоммонбуфферинлевел (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140487"
---
# <a name="avenccommonbufferinlevel-property"></a><span data-ttu-id="76eed-104">Авенккоммонбуфферинлевел, свойство</span><span class="sxs-lookup"><span data-stu-id="76eed-104">AVEncCommonBufferInLevel property</span></span>

<span data-ttu-id="76eed-105">Задает начальный уровень буфера кодирования в битах.</span><span class="sxs-lookup"><span data-stu-id="76eed-105">Specifies the initial level of the encoding buffer, in bits.</span></span> <span data-ttu-id="76eed-106">Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).</span><span class="sxs-lookup"><span data-stu-id="76eed-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="76eed-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="76eed-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="76eed-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="76eed-108">Data type</span></span>

<span data-ttu-id="76eed-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="76eed-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="76eed-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="76eed-110">Property GUID</span></span>

<span data-ttu-id="76eed-111">**КОДЕКАПИ \_ авенккоммонбуфферинлевел**</span><span class="sxs-lookup"><span data-stu-id="76eed-111">**CODECAPI\_AVEncCommonBufferInLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="76eed-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="76eed-112">Property value</span></span>

<span data-ttu-id="76eed-113">Это свойство имеет линейный Диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="76eed-113">This property has a linear range of values.</span></span> <span data-ttu-id="76eed-114">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="76eed-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="76eed-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76eed-115">Remarks</span></span>

<span data-ttu-id="76eed-116">Для видео в формате MPEG это свойство определяет заполнение исходной видеобуферной проверки (ВБВ).</span><span class="sxs-lookup"><span data-stu-id="76eed-116">For MPEG video, this property defines the initial video buffer verifier (VBV) fullness.</span></span> <span data-ttu-id="76eed-117">Он поддерживает объединение потоков во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="76eed-117">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="76eed-118">Требования</span><span class="sxs-lookup"><span data-stu-id="76eed-118">Requirements</span></span>



| <span data-ttu-id="76eed-119">Требование</span><span class="sxs-lookup"><span data-stu-id="76eed-119">Requirement</span></span> | <span data-ttu-id="76eed-120">Значение</span><span class="sxs-lookup"><span data-stu-id="76eed-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76eed-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76eed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="76eed-122">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="76eed-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="76eed-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76eed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="76eed-124">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="76eed-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="76eed-125">Header</span><span class="sxs-lookup"><span data-stu-id="76eed-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="76eed-126"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="76eed-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76eed-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76eed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76eed-128">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="76eed-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="76eed-129">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="76eed-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




