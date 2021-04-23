---
description: Указывает максимальное число кадров ссылок, поддерживаемое кодировщиком.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: Свойство CODECAPI_AVEncVideoMaxNumRefFrame (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157007"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a><span data-ttu-id="84b95-103">КОДЕКАПИ \_ авенквидеомакснумреффраме, свойство</span><span class="sxs-lookup"><span data-stu-id="84b95-103">CODECAPI\_AVEncVideoMaxNumRefFrame property</span></span>

<span data-ttu-id="84b95-104">Указывает максимальное число кадров ссылок, поддерживаемое кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="84b95-104">Specifies the maximum reference frames supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="84b95-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="84b95-105">Data type</span></span>

<span data-ttu-id="84b95-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="84b95-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="84b95-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="84b95-107">Property GUID</span></span>

<span data-ttu-id="84b95-108">**КОДЕКАПИ \_ авенквидеомакснумреффраме**</span><span class="sxs-lookup"><span data-stu-id="84b95-108">**CODECAPI\_AVEncVideoMaxNumRefFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="84b95-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84b95-109">Remarks</span></span>

<span data-ttu-id="84b95-110">Для H. 264 это соответствует параметру последовательности Set **Max \_ NUM \_ ref \_ frames** , как определено в спецификации H. 264.</span><span class="sxs-lookup"><span data-stu-id="84b95-110">For H.264, this maps to the Sequence Parameter Set variable **max\_num\_ref\_frames** as defined in H.264 specification.</span></span>

<span data-ttu-id="84b95-111">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="84b95-111">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="84b95-112">Кодировщики могут использовать меньше кадров ссылок для того, чтобы соблюдать уровень, указанный в битовый поток.</span><span class="sxs-lookup"><span data-stu-id="84b95-112">Encoders may use fewer reference frames in order to obey the level specified in the bitstream.</span></span>

<span data-ttu-id="84b95-113">Кодировщики должны поддерживать [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)и [**жетпараметерранжее**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="84b95-113">Encoders shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="84b95-114">Это статическое свойство означает, что его можно задать только до начала сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="84b95-114">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="84b95-115">Рекомендуемое значение по умолчанию — 2.</span><span class="sxs-lookup"><span data-stu-id="84b95-115">Recommended default value is 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="84b95-116">Требования</span><span class="sxs-lookup"><span data-stu-id="84b95-116">Requirements</span></span>



| <span data-ttu-id="84b95-117">Требование</span><span class="sxs-lookup"><span data-stu-id="84b95-117">Requirement</span></span> | <span data-ttu-id="84b95-118">Значение</span><span class="sxs-lookup"><span data-stu-id="84b95-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84b95-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84b95-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84b95-120">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="84b95-120">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="84b95-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84b95-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84b95-122">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="84b95-122">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="84b95-123">Header</span><span class="sxs-lookup"><span data-stu-id="84b95-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="84b95-124"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="84b95-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b95-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84b95-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b95-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84b95-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

