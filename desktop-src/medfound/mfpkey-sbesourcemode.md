---
description: Задает конфигурацию потока для источника мультимедиа ВТВ.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: Свойство MFPKEY_SBESourceMode (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991599"
---
# <a name="mfpkey_sbesourcemode-property"></a><span data-ttu-id="25ecc-103">МФПКЭЙ \_ сбесаурцемоде, свойство</span><span class="sxs-lookup"><span data-stu-id="25ecc-103">MFPKEY\_SBESourceMode property</span></span>

<span data-ttu-id="25ecc-104">Задает конфигурацию потока для источника мультимедиа ВТВ.</span><span class="sxs-lookup"><span data-stu-id="25ecc-104">Sets the stream configuration for the WTV media source.</span></span>



<span data-ttu-id="25ecc-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="25ecc-105">Data type</span></span>

<span data-ttu-id="25ecc-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="25ecc-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="25ecc-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="25ecc-107">PROPVARIANT member</span></span>

<span data-ttu-id="25ecc-108">**INT**</span><span class="sxs-lookup"><span data-stu-id="25ecc-108">**INT**</span></span>

<span data-ttu-id="25ecc-109">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="25ecc-109">VT\_INT</span></span>

<span data-ttu-id="25ecc-110">**интвал**</span><span class="sxs-lookup"><span data-stu-id="25ecc-110">**intVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="25ecc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25ecc-111">Remarks</span></span>

<span data-ttu-id="25ecc-112">Это свойство используется для настройки источника мультимедиа ВТВ.</span><span class="sxs-lookup"><span data-stu-id="25ecc-112">Use this property to configure the WTV media source.</span></span> <span data-ttu-id="25ecc-113">Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="25ecc-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="25ecc-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="25ecc-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="25ecc-115">Источник мультимедиа ВТВ считывает записанные телепередачи Windows (файлы ВТВ и MS-DRV).</span><span class="sxs-lookup"><span data-stu-id="25ecc-115">The WTV media source reads Windows Recorded TV Show (.wtv and .ms-drv) files.</span></span>

<span data-ttu-id="25ecc-116">Это свойство должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="25ecc-116">This property must have one of the following values.</span></span>

-   <span data-ttu-id="25ecc-117">1: сопоставьте доступные звуковые потоки с одним выходом на основе локальной системы.</span><span class="sxs-lookup"><span data-stu-id="25ecc-117">1: Map available audio streams to a single output, based on the system local.</span></span> <span data-ttu-id="25ecc-118">Этот режим подходит для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="25ecc-118">This mode is appropriate for playback.</span></span> <span data-ttu-id="25ecc-119">(по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="25ecc-119">(Default.)</span></span>
-   2. <span data-ttu-id="25ecc-120">Выбираются все звуковые потоки и подпотоки (например, заголовок и потоки данных).</span><span class="sxs-lookup"><span data-stu-id="25ecc-120">All audio streams and substreams (such as caption and data streams) are selected.</span></span> <span data-ttu-id="25ecc-121">Этот режим подходит для ремуксинг или кодирования.</span><span class="sxs-lookup"><span data-stu-id="25ecc-121">This mode is appropriate for remuxing or transcoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ecc-122">Требования</span><span class="sxs-lookup"><span data-stu-id="25ecc-122">Requirements</span></span>



| <span data-ttu-id="25ecc-123">Требование</span><span class="sxs-lookup"><span data-stu-id="25ecc-123">Requirement</span></span> | <span data-ttu-id="25ecc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="25ecc-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25ecc-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25ecc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="25ecc-126">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="25ecc-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="25ecc-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25ecc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="25ecc-128">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="25ecc-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="25ecc-129">Header</span><span class="sxs-lookup"><span data-stu-id="25ecc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="25ecc-130"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="25ecc-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25ecc-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25ecc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ecc-132">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25ecc-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
