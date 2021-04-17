---
description: Интерфейс Исамплеграббер предоставляется образцом фильтра захвата. Он позволяет приложению извлекать отдельные примеры мультимедиа по мере их перемещения через граф фильтра.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Интерфейс Исамплеграббер (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674848"
---
# <a name="isamplegrabber-interface"></a><span data-ttu-id="a88a9-104">Интерфейс Исамплеграббер</span><span class="sxs-lookup"><span data-stu-id="a88a9-104">ISampleGrabber interface</span></span>

> [!Note]  
> <span data-ttu-id="a88a9-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a88a9-105">\[Deprecated.</span></span> <span data-ttu-id="a88a9-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a88a9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a88a9-107">Интерфейс **исамплеграббер** предоставляется [**образцом фильтра захвата**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a88a9-107">The **ISampleGrabber** interface is exposed by the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="a88a9-108">Он позволяет приложению извлекать отдельные примеры мультимедиа по мере их перемещения через граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="a88a9-108">It enables an application to retrieve individual media samples as they move through the filter graph.</span></span>

## <a name="members"></a><span data-ttu-id="a88a9-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="a88a9-109">Members</span></span>

<span data-ttu-id="a88a9-110">Интерфейс **исамплеграббер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a88a9-110">The **ISampleGrabber** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a88a9-111">**Исамплеграббер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a88a9-111">**ISampleGrabber** also has these types of members:</span></span>

-   [<span data-ttu-id="a88a9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="a88a9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a88a9-113">Методы</span><span class="sxs-lookup"><span data-stu-id="a88a9-113">Methods</span></span>

<span data-ttu-id="a88a9-114">Интерфейс **исамплеграббер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a88a9-114">The **ISampleGrabber** interface has these methods.</span></span>



| <span data-ttu-id="a88a9-115">Метод</span><span class="sxs-lookup"><span data-stu-id="a88a9-115">Method</span></span>                                                                | <span data-ttu-id="a88a9-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a88a9-116">Description</span></span>                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a88a9-117">**жетконнектедмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="a88a9-117">**GetConnectedMediaType**</span></span>](isamplegrabber-getconnectedmediatype.md) | <span data-ttu-id="a88a9-118">Извлекает тип носителя для соединения со входным закреплением образца захвата.</span><span class="sxs-lookup"><span data-stu-id="a88a9-118">Retrieves the media type for the connection on the input pin of Sample Grabber.</span></span><br/>                                        |
| [<span data-ttu-id="a88a9-119">**жеткуррентбуффер**</span><span class="sxs-lookup"><span data-stu-id="a88a9-119">**GetCurrentBuffer**</span></span>](isamplegrabber-getcurrentbuffer.md)           | <span data-ttu-id="a88a9-120">Извлекает копию образца, который фильтр получил последним.</span><span class="sxs-lookup"><span data-stu-id="a88a9-120">Retrieves a copy of the sample that the filter received most recently.</span></span><br/>                                                 |
| [<span data-ttu-id="a88a9-121">**жеткуррентсампле**</span><span class="sxs-lookup"><span data-stu-id="a88a9-121">**GetCurrentSample**</span></span>](isamplegrabber-getcurrentsample.md)           | <span data-ttu-id="a88a9-122">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="a88a9-122">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="a88a9-123">**сетбуфферсамплес**</span><span class="sxs-lookup"><span data-stu-id="a88a9-123">**SetBufferSamples**</span></span>](isamplegrabber-setbuffersamples.md)           | <span data-ttu-id="a88a9-124">Указывает, следует ли копировать демонстрационные данные в буфер, так как он проходит через фильтр.</span><span class="sxs-lookup"><span data-stu-id="a88a9-124">Specifies whether to copy sample data into a buffer as it goes through the filter.</span></span><br/>                                     |
| [<span data-ttu-id="a88a9-125">**SetCallback**</span><span class="sxs-lookup"><span data-stu-id="a88a9-125">**SetCallback**</span></span>](isamplegrabber-setcallback.md)                     | <span data-ttu-id="a88a9-126">Указывает метод обратного вызова для вызова в входящих примерах.</span><span class="sxs-lookup"><span data-stu-id="a88a9-126">Specifies a callback method to call on incoming samples.</span></span><br/>                                                               |
| [<span data-ttu-id="a88a9-127">**сетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="a88a9-127">**SetMediaType**</span></span>](isamplegrabber-setmediatype.md)                   | <span data-ttu-id="a88a9-128">Указывает тип носителя для соединения во входном закрепление образца области захвата.</span><span class="sxs-lookup"><span data-stu-id="a88a9-128">Specifies the media type for the connection on the input pin of the Sample Grabber.</span></span><br/>                                    |
| [<span data-ttu-id="a88a9-129">**сетонешот**</span><span class="sxs-lookup"><span data-stu-id="a88a9-129">**SetOneShot**</span></span>](isamplegrabber-setoneshot.md)                       | <span data-ttu-id="a88a9-130">Указывает, останавливается ли фильтр [**захвата выборки**](sample-grabber-filter.md) после того, как фильтр получит образец.</span><span class="sxs-lookup"><span data-stu-id="a88a9-130">Specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a88a9-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a88a9-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a88a9-132">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="a88a9-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a88a9-133">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a88a9-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a88a9-134">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a88a9-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a88a9-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a88a9-135">Requirements</span></span>



| <span data-ttu-id="a88a9-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a88a9-136">Requirement</span></span> | <span data-ttu-id="a88a9-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a88a9-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a88a9-138">Header</span><span class="sxs-lookup"><span data-stu-id="a88a9-138">Header</span></span><br/>  | <dl> <span data-ttu-id="a88a9-139"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="a88a9-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a88a9-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a88a9-140">Library</span></span><br/> | <dl> <span data-ttu-id="a88a9-141"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a88a9-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a88a9-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a88a9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88a9-143">Использование образца захвата</span><span class="sxs-lookup"><span data-stu-id="a88a9-143">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 
