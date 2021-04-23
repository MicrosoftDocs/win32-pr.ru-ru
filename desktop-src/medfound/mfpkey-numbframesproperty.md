---
description: Задает число двунаправленных прогнозирующих кадров (B-кадров).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: Свойство MFPKEY_NUMBFRAMES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647283"
---
# <a name="mfpkey_numbframes-property"></a><span data-ttu-id="d805d-103">МФПКЭЙ \_ нумбфрамес, свойство</span><span class="sxs-lookup"><span data-stu-id="d805d-103">MFPKEY\_NUMBFRAMES Property</span></span>

<span data-ttu-id="d805d-104">Задает число двунаправленных прогнозирующих кадров (B-кадров).</span><span class="sxs-lookup"><span data-stu-id="d805d-104">Specifies the number of bidirectional predictive frames (B-frames).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d805d-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="d805d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d805d-106">g \_ всзвмвкнумбфрамес</span><span class="sxs-lookup"><span data-stu-id="d805d-106">g\_wszWMVCNumBFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="d805d-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d805d-107">Data Type</span></span>

<span data-ttu-id="d805d-108">VT-I4</span><span class="sxs-lookup"><span data-stu-id="d805d-108">VT-I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d805d-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d805d-109">Default Value</span></span>

<span data-ttu-id="d805d-110">0</span><span class="sxs-lookup"><span data-stu-id="d805d-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="d805d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d805d-111">Remarks</span></span>

<span data-ttu-id="d805d-112">По умолчанию в Windows Media Video 9 используются только интрафрамес (I-кадры), которые также называются ключевыми кадрами или закрепленными кадрами, которые являются полностью закодированными кадрами, и прогнозными кадрами (P-кадры), которые кодируются в отличие от предыдущего I-кадра.</span><span class="sxs-lookup"><span data-stu-id="d805d-112">By default, Windows Media Video 9 uses only intraframes (I-frames), also known as key frames or anchor frames, which are fully encoded frames, and predictive frames (P-frames), which are encoded as a difference from the previous I-frame.</span></span> <span data-ttu-id="d805d-113">B-кадры отличаются от кадров P-Frame, так как они сохраняют как различия предыдущего кадра, так и отличия от следующего кадра.</span><span class="sxs-lookup"><span data-stu-id="d805d-113">B-frames are different from P-frames because they store both the differences from the previous frame and the differences from the following frame.</span></span>

<span data-ttu-id="d805d-114">При настройке кодека для использования B-кадров он будет использовать указанное число кадров B-фреймов между каждой парой кадров любого типа I или P.</span><span class="sxs-lookup"><span data-stu-id="d805d-114">When you configure the codec to uses B-frames, it will use the specified number of B-frames between each pair of frames of either I or P type.</span></span>

<span data-ttu-id="d805d-115">Например, если последовательность кадров без кадров "B" имеет значение "ИППППППППИ", то одинаковое кодирование последовательности с двумя кадрами B — "ИББПББПББИ".</span><span class="sxs-lookup"><span data-stu-id="d805d-115">For example, if a sequence of frames without B-frames is "IPPPPPPPPI" then the same sequence encoding with two B-frames would be "IBBPBBPBBI".</span></span>

<span data-ttu-id="d805d-116">Для большинства содержимого подходят один или два кадра в виде «B-кадров».</span><span class="sxs-lookup"><span data-stu-id="d805d-116">For most content either one or two B-frames are appropriate.</span></span> <span data-ttu-id="d805d-117">При более высоких скоростях данных один B-кадр обычно является оптимальным выбором.</span><span class="sxs-lookup"><span data-stu-id="d805d-117">At higher data rates, one B-frame is normally the optimal choice.</span></span> <span data-ttu-id="d805d-118">Три или более редко полезны.</span><span class="sxs-lookup"><span data-stu-id="d805d-118">Three or more are rarely useful.</span></span>

<span data-ttu-id="d805d-119">Допустимый диапазон значений для этого свойства — от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="d805d-119">The valid range of values for this property is 0 to 7.</span></span>

## <a name="requirements"></a><span data-ttu-id="d805d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d805d-120">Requirements</span></span>



| <span data-ttu-id="d805d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d805d-121">Requirement</span></span> | <span data-ttu-id="d805d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d805d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d805d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d805d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d805d-124">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d805d-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d805d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d805d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d805d-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d805d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d805d-127">Header</span><span class="sxs-lookup"><span data-stu-id="d805d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d805d-128"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d805d-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d805d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d805d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d805d-130">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d805d-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




