---
description: Управляет сигнализацией Мфсампликстенсион \_ меанабсолутедифференце через имфаттрибуте для каждого выходного образца.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: Свойство CODECAPI_AVEncVideoMeanAbsoluteDifference (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692077"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a><span data-ttu-id="5ae77-103">КОДЕКАПИ \_ авенквидеомеанабсолутедифференце, свойство</span><span class="sxs-lookup"><span data-stu-id="5ae77-103">CODECAPI\_AVEncVideoMeanAbsoluteDifference property</span></span>

<span data-ttu-id="5ae77-104">Управляет сигнализацией [мфсампликстенсион \_ Меанабсолутедифференце](mfsampleextension-meanabsolutedifference.md) через [**имфаттрибуте**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для каждого выходного образца.</span><span class="sxs-lookup"><span data-stu-id="5ae77-104">Controls the signaling of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) through [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) on each output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="5ae77-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5ae77-105">Data type</span></span>

<span data-ttu-id="5ae77-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="5ae77-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5ae77-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="5ae77-107">Property GUID</span></span>

<span data-ttu-id="5ae77-108">**КОДЕКАПИ \_ авенквидеомеанабсолутедифференце**</span><span class="sxs-lookup"><span data-stu-id="5ae77-108">**CODECAPI\_AVEncVideoMeanAbsoluteDifference**</span></span>

## <a name="remarks"></a><span data-ttu-id="5ae77-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ae77-109">Remarks</span></span>

<span data-ttu-id="5ae77-110">Если приложение устанавливает ненулевое значение, кодировщику следует добавить к каждому выходному примеру атрибут [мфсампликстенсион \_ меанабсолутедифференце](mfsampleextension-meanabsolutedifference.md) Sample.</span><span class="sxs-lookup"><span data-stu-id="5ae77-110">If the application sets a non-zero value then the encoder should add the [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sample attribute to each output sample.</span></span> <span data-ttu-id="5ae77-111">Атрибут Мфсампликстенсион \_ меанабсолутедифференце показывает среднее абсолютное различие между исходными примерами и прогнозируемыми примерами на плоскости Y.</span><span class="sxs-lookup"><span data-stu-id="5ae77-111">The MFSampleExtension\_MeanAbsoluteDifference attribute indicates the mean absolute difference between the source samples and the predicted samples in the Y plane.</span></span>

<span data-ttu-id="5ae77-112">Если кодировщик возвращает 0 для **жетпараметерранже**, кодировщик не поддерживает выходные данные [мфсампликстенсион \_ меанабсолутедифференце](mfsampleextension-meanabsolutedifference.md) в выходных образцах.</span><span class="sxs-lookup"><span data-stu-id="5ae77-112">If the encoder returns 0 for **GetParameterRange**, then the encoder does not support the output of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) on the output samples.</span></span>

<span data-ttu-id="5ae77-113">Значение по умолчанию должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="5ae77-113">The default value should be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ae77-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5ae77-114">Requirements</span></span>



| <span data-ttu-id="5ae77-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5ae77-115">Requirement</span></span> | <span data-ttu-id="5ae77-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5ae77-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae77-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ae77-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae77-118">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ae77-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5ae77-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ae77-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae77-120">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ae77-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5ae77-121">Header</span><span class="sxs-lookup"><span data-stu-id="5ae77-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ae77-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ae77-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ae77-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ae77-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae77-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5ae77-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




