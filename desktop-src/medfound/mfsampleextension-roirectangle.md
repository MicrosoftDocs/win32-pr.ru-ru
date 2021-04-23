---
description: Задает границы интересующей области, указывающие регион кадра, для которого требуется другое качество.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: Атрибут MFSampleExtension_ROIRectangle (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719468"
---
# <a name="mfsampleextension_roirectangle-attribute"></a><span data-ttu-id="e6156-103">Мфсампликстенсион \_ роиректангле, атрибут</span><span class="sxs-lookup"><span data-stu-id="e6156-103">MFSampleExtension\_ROIRectangle attribute</span></span>

<span data-ttu-id="e6156-104">Задает границы интересующей области, указывающие регион кадра, для которого требуется другое качество.</span><span class="sxs-lookup"><span data-stu-id="e6156-104">Specifies the bounds of the region of interest which indicates the region of the frame that requires different quality.</span></span>

## <a name="data-type"></a><span data-ttu-id="e6156-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e6156-105">Data type</span></span>

<span data-ttu-id="e6156-106">**[**Рентабельность инвестиций \_ ОБЛАСТЬ**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** хранится в виде **большого двоичного объекта**</span><span class="sxs-lookup"><span data-stu-id="e6156-106">**[**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** stored as **BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="e6156-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6156-107">Remarks</span></span>

<span data-ttu-id="e6156-108">После успешной установки [кодекапи \_ авенквидеороиенаблед](codecapi-avencvideoroienabled.md) на ненулевое значение в файле MFT кодировщика приложение может установить этот атрибут для входных примеров и предполагать, что он будет учитываться.</span><span class="sxs-lookup"><span data-stu-id="e6156-108">After successfully setting [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) to a non-zero value on an encoder MFT, the application can set this attribute on input samples and expect it to be honored.</span></span>

<span data-ttu-id="e6156-109">Если для [кодекапи \_ авенквидеороиенаблед](codecapi-avencvideoroienabled.md) не задано ненулевое значение, то атрибут мфсампликстенсион \_ роиректангле игнорируется во входных примерах.</span><span class="sxs-lookup"><span data-stu-id="e6156-109">If [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) is not set to a non-zero value, the MFSampleExtension\_ROIRectangle attribute is ignored on input samples.</span></span>

<span data-ttu-id="e6156-110">Мфсампликстенсион \_ роиректангле устанавливается на входном образце и применяется только к текущему входному образцу.</span><span class="sxs-lookup"><span data-stu-id="e6156-110">MFSampleExtension\_ROIRectangle is set on an input sample and is only applied to the current input sample.</span></span>

<span data-ttu-id="e6156-111">Поле **кпделта** в структуре [**\_ области рентабельности**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) определяет Дельта параметра дискретизация для указанной области из оставшейся части кадра.</span><span class="sxs-lookup"><span data-stu-id="e6156-111">The **QPDelta** field on the [**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) structure specifies the quantization parameter delta for the specified region from the rest of the frame.</span></span> <span data-ttu-id="e6156-112">Если **кпделта** имеет положительное значение, это означает, что приложение хочет, чтобы прямоугольник имел более низкое качество, чем остальная часть кадра.</span><span class="sxs-lookup"><span data-stu-id="e6156-112">If **QPDelta** is positive, this indicates the application wants the rectangle to have lower quality than the rest of the frame.</span></span>

<span data-ttu-id="e6156-113">**Кодировщики H. 264/AVC:** **кпделта** должны быть в диапазоне от \[ -25 до + 25 \] .</span><span class="sxs-lookup"><span data-stu-id="e6156-113">**H.264/AVC encoders:** **QPDelta** shall be between \[-25, +25\].</span></span> <span data-ttu-id="e6156-114">Кодировщик должен убедиться, что последний обработчик QP находится в допустимом диапазоне для видео Standard.</span><span class="sxs-lookup"><span data-stu-id="e6156-114">The encoder shall ensure that the final QP is in a valid range for the video standard.</span></span>

<span data-ttu-id="e6156-115">Для указанной области не требуется выровняйте по МБ.</span><span class="sxs-lookup"><span data-stu-id="e6156-115">The specified region is not required to be MB aligned.</span></span> <span data-ttu-id="e6156-116">Кодировщики имеют гибкие возможности для выбора фактической границы.</span><span class="sxs-lookup"><span data-stu-id="e6156-116">Encoders have flexibility to decide the actual boundary.</span></span> <span data-ttu-id="e6156-117">Рекомендуется охватывать весь указанный регион.</span><span class="sxs-lookup"><span data-stu-id="e6156-117">It is recommended to cover the entire specified region.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6156-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e6156-118">Requirements</span></span>



| <span data-ttu-id="e6156-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e6156-119">Requirement</span></span> | <span data-ttu-id="e6156-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e6156-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e6156-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6156-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e6156-122">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="e6156-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="e6156-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6156-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e6156-124">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e6156-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e6156-125">Header</span><span class="sxs-lookup"><span data-stu-id="e6156-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6156-126"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6156-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6156-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6156-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6156-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e6156-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




