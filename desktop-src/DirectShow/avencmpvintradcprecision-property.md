---
description: Указывает точность коэффициентов контроллеров домена в битах. Это свойство применяется к кодировщикам видео MPEG.
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: Свойство АвенкмпвинтрадкпреЦисион (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d4bdd3c08f49586eb2663829271ae4166d917e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894813"
---
# <a name="avencmpvintradcprecision-property"></a><span data-ttu-id="2680e-104">АвенкмпвинтрадкпреЦисион, свойство</span><span class="sxs-lookup"><span data-stu-id="2680e-104">AVEncMPVIntraDCPrecision property</span></span>

<span data-ttu-id="2680e-105">Указывает точность коэффициентов контроллеров домена в битах.</span><span class="sxs-lookup"><span data-stu-id="2680e-105">Specifies the precision of the DC coefficients, in bits.</span></span> <span data-ttu-id="2680e-106">Это свойство применяется к кодировщикам видео MPEG.</span><span class="sxs-lookup"><span data-stu-id="2680e-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="2680e-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2680e-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2680e-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2680e-108">Data type</span></span>

<span data-ttu-id="2680e-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="2680e-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2680e-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="2680e-110">Property GUID</span></span>

<span data-ttu-id="2680e-111">**КОДЕКАПИ \_ авенкмпвинтрадкпреЦисион**</span><span class="sxs-lookup"><span data-stu-id="2680e-111">**CODECAPI\_AVEncMPVIntraDCPrecision**</span></span>

## <a name="property-value"></a><span data-ttu-id="2680e-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2680e-112">Property value</span></span>

<span data-ttu-id="2680e-113">Это свойство имеет линейный Диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="2680e-113">This property has a linear range of values.</span></span> <span data-ttu-id="2680e-114">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="2680e-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="2680e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2680e-115">Remarks</span></span>

<span data-ttu-id="2680e-116">Обычный диапазон для этого свойства — от 8 до 11 бит.</span><span class="sxs-lookup"><span data-stu-id="2680e-116">The usual range for this property is 8 to 11 bits.</span></span> <span data-ttu-id="2680e-117">Если значение равно нулю, кодировщик выбирает точность.</span><span class="sxs-lookup"><span data-stu-id="2680e-117">If the value is zero, the encoder selects the precision.</span></span>

## <a name="requirements"></a><span data-ttu-id="2680e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2680e-118">Requirements</span></span>



| <span data-ttu-id="2680e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2680e-119">Requirement</span></span> | <span data-ttu-id="2680e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2680e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2680e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2680e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2680e-122">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2680e-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2680e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2680e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2680e-124">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="2680e-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2680e-125">Header</span><span class="sxs-lookup"><span data-stu-id="2680e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2680e-126"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2680e-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2680e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2680e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2680e-128">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="2680e-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2680e-129">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="2680e-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




