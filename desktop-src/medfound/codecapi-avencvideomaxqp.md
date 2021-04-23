---
description: Указывает максимальный поддерживаемый кодировщиком обработчик запросов.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: Свойство CODECAPI_AVEncVideoMaxQP (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692078"
---
# <a name="codecapi_avencvideomaxqp-property"></a><span data-ttu-id="4a189-103">КОДЕКАПИ \_ авенквидеомакскп, свойство</span><span class="sxs-lookup"><span data-stu-id="4a189-103">CODECAPI\_AVEncVideoMaxQP property</span></span>

<span data-ttu-id="4a189-104">Указывает максимальный поддерживаемый кодировщиком обработчик запросов.</span><span class="sxs-lookup"><span data-stu-id="4a189-104">Specifies the maximum QP supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a189-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4a189-105">Data type</span></span>

<span data-ttu-id="4a189-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="4a189-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4a189-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="4a189-107">Property GUID</span></span>

<span data-ttu-id="4a189-108">**КОДЕКАПИ \_ авенквидеомакскп**</span><span class="sxs-lookup"><span data-stu-id="4a189-108">**CODECAPI\_AVEncVideoMaxQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="4a189-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a189-109">Remarks</span></span>

<span data-ttu-id="4a189-110">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="4a189-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="4a189-111">Кодировщик должен поддерживать [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)и [**жетпараметерранже**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="4a189-111">The encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="4a189-112">Это статическое свойство означает, что его можно задать только до начала сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="4a189-112">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="4a189-113">Значение по умолчанию должно быть максимальным числом запросов QP, разрешенным соответствующим стандартом кодирования.</span><span class="sxs-lookup"><span data-stu-id="4a189-113">Default value shall be the max QP allowed by the corresponding coding standard.</span></span> <span data-ttu-id="4a189-114">Например, кодировщики H. 264 должны иметь значение по умолчанию 51.</span><span class="sxs-lookup"><span data-stu-id="4a189-114">For example, H.264 encoders shall have a default value of 51.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a189-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4a189-115">Requirements</span></span>



| <span data-ttu-id="4a189-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4a189-116">Requirement</span></span> | <span data-ttu-id="4a189-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4a189-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a189-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a189-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4a189-119">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="4a189-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="4a189-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a189-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4a189-121">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="4a189-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4a189-122">Header</span><span class="sxs-lookup"><span data-stu-id="4a189-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a189-123"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a189-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a189-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a189-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a189-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a189-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4a189-126">КОДЕКАПИ \_ авенквидеоминкп</span><span class="sxs-lookup"><span data-stu-id="4a189-126">CODECAPI\_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
</dt> </dl>

 

