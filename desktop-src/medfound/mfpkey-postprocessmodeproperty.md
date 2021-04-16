---
description: Задает режим обработки, выполняемый для декодера.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: Свойство MFPKEY_POSTPROCESSMODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708586"
---
# <a name="mfpkey_postprocessmode-property"></a><span data-ttu-id="66b19-103">МФПКЭЙ \_ постпроцессмоде, свойство</span><span class="sxs-lookup"><span data-stu-id="66b19-103">MFPKEY\_POSTPROCESSMODE Property</span></span>

<span data-ttu-id="66b19-104">Задает режим обработки, выполняемый для декодера.</span><span class="sxs-lookup"><span data-stu-id="66b19-104">Specifies the post processing mode for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="66b19-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="66b19-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="66b19-106">**g \_ всзвмвкфорцепостпроцессмоде**</span><span class="sxs-lookup"><span data-stu-id="66b19-106">**g\_wszWMVCForcePostProcessMode**</span></span>

## <a name="data-type"></a><span data-ttu-id="66b19-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="66b19-107">Data Type</span></span>

<span data-ttu-id="66b19-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="66b19-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="66b19-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66b19-109">Remarks</span></span>

<span data-ttu-id="66b19-110">Присвойте этому свойству одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="66b19-110">Set this property to one of the following values.</span></span>



| <span data-ttu-id="66b19-111">Значение</span><span class="sxs-lookup"><span data-stu-id="66b19-111">Value</span></span> | <span data-ttu-id="66b19-112">Значение</span><span class="sxs-lookup"><span data-stu-id="66b19-112">Meaning</span></span>                                                                                |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66b19-113">-1</span><span class="sxs-lookup"><span data-stu-id="66b19-113">-1</span></span>    | <span data-ttu-id="66b19-114">Декодер устанавливает режим последующей обработки на основе доступных ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="66b19-114">The decoder sets the post processing mode adaptively based on available CPU resources.</span></span> |
| <span data-ttu-id="66b19-115">0</span><span class="sxs-lookup"><span data-stu-id="66b19-115">0</span></span>     | <span data-ttu-id="66b19-116">Декодер не выполняет обработку после обработки.</span><span class="sxs-lookup"><span data-stu-id="66b19-116">The decoder performs no post processing.</span></span>                                               |
| <span data-ttu-id="66b19-117">1</span><span class="sxs-lookup"><span data-stu-id="66b19-117">1</span></span>     | <span data-ttu-id="66b19-118">декодер фсе выполняет быстрое деблокирование.</span><span class="sxs-lookup"><span data-stu-id="66b19-118">fThe decoder performs fast deblocking.</span></span>                                                 |
| <span data-ttu-id="66b19-119">2</span><span class="sxs-lookup"><span data-stu-id="66b19-119">2</span></span>     | <span data-ttu-id="66b19-120">Декодер выполняет полное деблокирование.</span><span class="sxs-lookup"><span data-stu-id="66b19-120">The decoder performs full deblocking.</span></span>                                                  |
| <span data-ttu-id="66b19-121">3</span><span class="sxs-lookup"><span data-stu-id="66b19-121">3</span></span>     | <span data-ttu-id="66b19-122">Декодер выполняет быстрое деблокировку и отдачу.</span><span class="sxs-lookup"><span data-stu-id="66b19-122">The decoder performs fast deblocking and deringing.</span></span>                                    |
| <span data-ttu-id="66b19-123">4</span><span class="sxs-lookup"><span data-stu-id="66b19-123">4</span></span>     | <span data-ttu-id="66b19-124">Декодер выполняет полное деблокирование и выдачу.</span><span class="sxs-lookup"><span data-stu-id="66b19-124">The decoder performs full deblocking and deringing.</span></span>                                    |



 

<span data-ttu-id="66b19-125">Так как значение этого свойства переходит от 0 до 4, сложность декодирования, использование ресурсов ЦП и увеличение качества изображения.</span><span class="sxs-lookup"><span data-stu-id="66b19-125">As the value of this property goes from 0 to 4, the decoding complexity, use of CPU resources, and picture quality all increase.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b19-126">Требования</span><span class="sxs-lookup"><span data-stu-id="66b19-126">Requirements</span></span>



| <span data-ttu-id="66b19-127">Требование</span><span class="sxs-lookup"><span data-stu-id="66b19-127">Requirement</span></span> | <span data-ttu-id="66b19-128">Значение</span><span class="sxs-lookup"><span data-stu-id="66b19-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66b19-129">Клиент</span><span class="sxs-lookup"><span data-stu-id="66b19-129">Client</span></span><br/> | <span data-ttu-id="66b19-130">Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="66b19-130">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="66b19-131">Header</span><span class="sxs-lookup"><span data-stu-id="66b19-131">Header</span></span><br/> | <dl> <span data-ttu-id="66b19-132"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b19-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66b19-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66b19-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b19-134">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66b19-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




