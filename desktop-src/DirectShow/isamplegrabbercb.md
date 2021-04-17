---
description: 'Интерфейс Исамплеграбберкб предоставляет методы обратного вызова для метода Исамплеграббер:: Сеткаллбакк. Если приложение вызывает этот метод, он должен реализовать этот интерфейс. Дополнительные сведения см. в разделе Исамплеграббер.'
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Интерфейс Исамплеграбберкб (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675177"
---
# <a name="isamplegrabbercb-interface"></a><span data-ttu-id="dc9df-105">Интерфейс Исамплеграбберкб</span><span class="sxs-lookup"><span data-stu-id="dc9df-105">ISampleGrabberCB interface</span></span>

> [!Note]  
> <span data-ttu-id="dc9df-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="dc9df-106">\[Deprecated.</span></span> <span data-ttu-id="dc9df-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc9df-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dc9df-108">`ISampleGrabberCB`Интерфейс предоставляет методы обратного вызова для метода [**исамплеграббер:: сеткаллбакк**](isamplegrabber-setcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="dc9df-108">The `ISampleGrabberCB` interface provides callback methods for the [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) method.</span></span> <span data-ttu-id="dc9df-109">Если приложение вызывает этот метод, он должен реализовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="dc9df-109">If your application calls that method, it must implement this interface.</span></span> <span data-ttu-id="dc9df-110">Дополнительные сведения см. в разделе [**исамплеграббер**](isamplegrabber.md).</span><span class="sxs-lookup"><span data-stu-id="dc9df-110">For more information, see [**ISampleGrabber**](isamplegrabber.md).</span></span>

## <a name="members"></a><span data-ttu-id="dc9df-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="dc9df-111">Members</span></span>

<span data-ttu-id="dc9df-112">Интерфейс **исамплеграбберкб** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dc9df-112">The **ISampleGrabberCB** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dc9df-113">**Исамплеграбберкб** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dc9df-113">**ISampleGrabberCB** also has these types of members:</span></span>

-   [<span data-ttu-id="dc9df-114">Методы</span><span class="sxs-lookup"><span data-stu-id="dc9df-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dc9df-115">Методы</span><span class="sxs-lookup"><span data-stu-id="dc9df-115">Methods</span></span>

<span data-ttu-id="dc9df-116">Интерфейс **исамплеграбберкб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dc9df-116">The **ISampleGrabberCB** interface has these methods.</span></span>



| <span data-ttu-id="dc9df-117">Метод</span><span class="sxs-lookup"><span data-stu-id="dc9df-117">Method</span></span>                                        | <span data-ttu-id="dc9df-118">Описание</span><span class="sxs-lookup"><span data-stu-id="dc9df-118">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="dc9df-119">**буфферкб**</span><span class="sxs-lookup"><span data-stu-id="dc9df-119">**BufferCB**</span></span>](isamplegrabbercb-buffercb.md) | <span data-ttu-id="dc9df-120">Метод обратного вызова, который получает указатель на образец буфера.</span><span class="sxs-lookup"><span data-stu-id="dc9df-120">Callback method that receives a pointer to the sample buffer.</span></span><br/> |
| [<span data-ttu-id="dc9df-121">**самплекб**</span><span class="sxs-lookup"><span data-stu-id="dc9df-121">**SampleCB**</span></span>](isamplegrabbercb-samplecb.md) | <span data-ttu-id="dc9df-122">Метод обратного вызова, который получает указатель на пример носителя.</span><span class="sxs-lookup"><span data-stu-id="dc9df-122">Callback method that receives a pointer to the media sample.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="dc9df-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc9df-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dc9df-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="dc9df-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dc9df-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc9df-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dc9df-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dc9df-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dc9df-127">Требования</span><span class="sxs-lookup"><span data-stu-id="dc9df-127">Requirements</span></span>



| <span data-ttu-id="dc9df-128">Требование</span><span class="sxs-lookup"><span data-stu-id="dc9df-128">Requirement</span></span> | <span data-ttu-id="dc9df-129">Значение</span><span class="sxs-lookup"><span data-stu-id="dc9df-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9df-130">Header</span><span class="sxs-lookup"><span data-stu-id="dc9df-130">Header</span></span><br/>  | <dl> <span data-ttu-id="dc9df-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc9df-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dc9df-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc9df-132">Library</span></span><br/> | <dl> <span data-ttu-id="dc9df-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc9df-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
