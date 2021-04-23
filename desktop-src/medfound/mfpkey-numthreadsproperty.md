---
description: Указывает число потоков, которые будет использовать кодировщик.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: Свойство MFPKEY_NUMTHREADS (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544911"
---
# <a name="mfpkey_numthreads-property"></a><span data-ttu-id="a6b5c-103">МФПКЭЙ \_ NUMTHREADS, свойство</span><span class="sxs-lookup"><span data-stu-id="a6b5c-103">MFPKEY\_NUMTHREADS Property</span></span>

<span data-ttu-id="a6b5c-104">Указывает число потоков, которые будет использовать кодировщик.</span><span class="sxs-lookup"><span data-stu-id="a6b5c-104">Specifies the number of threads that the encoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a6b5c-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="a6b5c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a6b5c-106">g \_ всзвмвкнумсреадс</span><span class="sxs-lookup"><span data-stu-id="a6b5c-106">g\_wszWMVCNumThreads</span></span>

## <a name="data-type"></a><span data-ttu-id="a6b5c-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a6b5c-107">Data Type</span></span>

<span data-ttu-id="a6b5c-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a6b5c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a6b5c-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a6b5c-109">Default Value</span></span>

<span data-ttu-id="a6b5c-110">1</span><span class="sxs-lookup"><span data-stu-id="a6b5c-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="a6b5c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6b5c-111">Remarks</span></span>

<span data-ttu-id="a6b5c-112">Это значение предназначено для разделения кодирования на несколько потоков, чтобы использовать преимущества компьютеров с несколькими процессорами.</span><span class="sxs-lookup"><span data-stu-id="a6b5c-112">This value is intended to divide encoding into multiple threads to take advantage of computers with multiple processors.</span></span> <span data-ttu-id="a6b5c-113">Разделение задач кодирования на несколько потоков может привести к незначительному снижению качества по сравнению с одним потоком.</span><span class="sxs-lookup"><span data-stu-id="a6b5c-113">Splitting encoding tasks into multiple threads can cause a slight decrease in quality as compared to a single thread.</span></span>

<span data-ttu-id="a6b5c-114">Для видеокодировщика (wmvencod.dll), выпущенного в Windows XP и Windows Vista, этому свойству должно быть присвоено значение 1, 2 или 4.</span><span class="sxs-lookup"><span data-stu-id="a6b5c-114">For the video encoder (wmvencod.dll) released with Windows XP and Windows Vista, this property should be set to 1, 2, or 4.</span></span> <span data-ttu-id="a6b5c-115">Другие значения будут округляться вниз.</span><span class="sxs-lookup"><span data-stu-id="a6b5c-115">Other values will be rounded down.</span></span>

<span data-ttu-id="a6b5c-116">Для видеокодировщика (wmvencod.dll), выпущенного в Windows 7, этому свойству должно быть присвоено значение 1, 2, 4 или 8.</span><span class="sxs-lookup"><span data-stu-id="a6b5c-116">For the video encoder (wmvencod.dll) released with Windows 7, this property should be set to 1, 2, 4, or 8.</span></span> <span data-ttu-id="a6b5c-117">Другие значения будут округляться вниз.</span><span class="sxs-lookup"><span data-stu-id="a6b5c-117">Other values will be rounded down.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6b5c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a6b5c-118">Requirements</span></span>



| <span data-ttu-id="a6b5c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a6b5c-119">Requirement</span></span> | <span data-ttu-id="a6b5c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a6b5c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b5c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6b5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6b5c-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a6b5c-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a6b5c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6b5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6b5c-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6b5c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a6b5c-125">Header</span><span class="sxs-lookup"><span data-stu-id="a6b5c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6b5c-126"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6b5c-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6b5c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6b5c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b5c-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6b5c-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




