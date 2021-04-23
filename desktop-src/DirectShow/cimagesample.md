---
description: Класс Цимажесампле реализует пример носителя, который управляет независимым от устройства точечным рисунком GDI (DIB).
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Класс Цимажесампле (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674937"
---
# <a name="cimagesample-class"></a><span data-ttu-id="662a6-103">Класс Цимажесампле</span><span class="sxs-lookup"><span data-stu-id="662a6-103">CImageSample class</span></span>

![Иерархия классов Цимажесампле](images/wutil03.png)

<span data-ttu-id="662a6-105">`CImageSample`Класс реализует пример носителя, который управляет независимым от устройства точечным рисунком GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="662a6-105">The `CImageSample` class implements a media sample that manages a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="662a6-106">Этот класс является производным от класса [**кмедиасампле**](cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="662a6-106">This class derives from the [**CMediaSample**](cmediasample.md) class.</span></span> <span data-ttu-id="662a6-107">Он предназначен для использования с классом [**Цимажеаллокатор**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="662a6-107">It is intended to be used with the [**CImageAllocator**](cimageallocator.md) class.</span></span> <span data-ttu-id="662a6-108">Класс **Цимажеаллокатор** предоставляет распределитель, создающий `CImageSample` объекты.</span><span class="sxs-lookup"><span data-stu-id="662a6-108">The **CImageAllocator** class provides an allocator that creates `CImageSample` objects.</span></span>



| <span data-ttu-id="662a6-109">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="662a6-109">Protected Member Variables</span></span>                        | <span data-ttu-id="662a6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="662a6-110">Description</span></span>                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="662a6-111">**m \_ дибдата**</span><span class="sxs-lookup"><span data-stu-id="662a6-111">**m\_DibData**</span></span>](cimagesample-m-dibdata.md)      | <span data-ttu-id="662a6-112">Содержит сведения о соотношении DIB, которым управляет этот объект.</span><span class="sxs-lookup"><span data-stu-id="662a6-112">Contains information about the DIB that this object is managing.</span></span>  |
| [<span data-ttu-id="662a6-113">**m \_ Бинит**</span><span class="sxs-lookup"><span data-stu-id="662a6-113">**m\_bInit**</span></span>](cimagesample-m-binit.md)          | <span data-ttu-id="662a6-114">Указывает, инициализирован ли объект.</span><span class="sxs-lookup"><span data-stu-id="662a6-114">Indicates whether the object has been initialized.</span></span>                |
| <span data-ttu-id="662a6-115">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="662a6-115">Public Methods</span></span>                                    | <span data-ttu-id="662a6-116">Описание</span><span class="sxs-lookup"><span data-stu-id="662a6-116">Description</span></span>                                                       |
| [<span data-ttu-id="662a6-117">**Цимажесампле**</span><span class="sxs-lookup"><span data-stu-id="662a6-117">**CImageSample**</span></span>](cimagesample-cimagesample.md) | <span data-ttu-id="662a6-118">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="662a6-118">Constructor method.</span></span>                                               |
| [<span data-ttu-id="662a6-119">**жетдибдата**</span><span class="sxs-lookup"><span data-stu-id="662a6-119">**GetDIBData**</span></span>](cimagesample-getdibdata.md)     | <span data-ttu-id="662a6-120">Извлекает сведения о соотношении DIB, которым управляет этот объект.</span><span class="sxs-lookup"><span data-stu-id="662a6-120">Retrieves information about the DIB that this object is managing.</span></span> |
| [<span data-ttu-id="662a6-121">**сетдибдата**</span><span class="sxs-lookup"><span data-stu-id="662a6-121">**SetDIBData**</span></span>](cimagesample-setdibdata.md)     | <span data-ttu-id="662a6-122">Задает сведения о соотношении DIB, которым управляет этот объект.</span><span class="sxs-lookup"><span data-stu-id="662a6-122">Sets information about the DIB that this object is managing.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="662a6-123">Требования</span><span class="sxs-lookup"><span data-stu-id="662a6-123">Requirements</span></span>



| <span data-ttu-id="662a6-124">Требование</span><span class="sxs-lookup"><span data-stu-id="662a6-124">Requirement</span></span> | <span data-ttu-id="662a6-125">Значение</span><span class="sxs-lookup"><span data-stu-id="662a6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="662a6-126">Header</span><span class="sxs-lookup"><span data-stu-id="662a6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="662a6-127"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="662a6-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="662a6-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="662a6-128">Library</span></span><br/> | <dl> <span data-ttu-id="662a6-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="662a6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




