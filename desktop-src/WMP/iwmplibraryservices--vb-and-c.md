---
title: Интерфейс Ивмплибрарисервицес (VB и C) (WMP. h)
description: Предоставляет методы для перечисления библиотек.
ms.assetid: f2a72731-6e61-4f78-b0ca-ae907004eb7d
keywords:
- Ивмплибрарисервицес (VB и C) интерфейс проигрывателя Windows Media
- Ивмплибрарисервицес (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPLibraryServices (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3493d5c94dcbd9db1e4f281a8fddfadbd2e336f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685204"
---
# <a name="iwmplibraryservices-vb-and-c-interface"></a><span data-ttu-id="67035-105">Интерфейс Ивмплибрарисервицес (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="67035-105">IWMPLibraryServices (VB and C#) interface</span></span>

<span data-ttu-id="67035-106">Предоставляет методы для перечисления библиотек.</span><span class="sxs-lookup"><span data-stu-id="67035-106">Provides methods to enumerate libraries.</span></span>

## <a name="members"></a><span data-ttu-id="67035-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="67035-107">Members</span></span>

<span data-ttu-id="67035-108">Интерфейс **ивмплибрарисервицес (VB и C#)** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="67035-108">The **IWMPLibraryServices (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="67035-109">Методы</span><span class="sxs-lookup"><span data-stu-id="67035-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67035-110">Методы</span><span class="sxs-lookup"><span data-stu-id="67035-110">Methods</span></span>

<span data-ttu-id="67035-111">Интерфейс **ивмплибрарисервицес (VB и C#)** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="67035-111">The **IWMPLibraryServices (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="67035-112">Метод</span><span class="sxs-lookup"><span data-stu-id="67035-112">Method</span></span>                                                                                               | <span data-ttu-id="67035-113">Описание</span><span class="sxs-lookup"><span data-stu-id="67035-113">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67035-114">**жеткаунтбитипе**</span><span class="sxs-lookup"><span data-stu-id="67035-114">**getCountByType**</span></span>](wmplibiwmplibraryservices-iwmplibraryservices-getcountbytype--vb-and-c.md)     | <span data-ttu-id="67035-115">Возвращает число доступных библиотек указанного типа.</span><span class="sxs-lookup"><span data-stu-id="67035-115">Returns the count of available libraries of a specified type.</span></span><br/>                                           |
| [<span data-ttu-id="67035-116">**жетлибрарибитипе**</span><span class="sxs-lookup"><span data-stu-id="67035-116">**getLibraryByType**</span></span>](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md) | <span data-ttu-id="67035-117">Возвращает интерфейс **ивмплибрари** , представляющий библиотеку с указанным типом и индексом.</span><span class="sxs-lookup"><span data-stu-id="67035-117">Returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span><br/> |



 

<span data-ttu-id="67035-118">Получите интерфейс **ивмплибрарисервицес** путем приведения объекта, возвращенного методом **аксвиндовсмедиаплайер. жетоккс** .</span><span class="sxs-lookup"><span data-stu-id="67035-118">Get an **IWMPLibraryServices** interface by casting the object returned from the **AxWindowsMediaPlayer.GetOcx** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="67035-119">Требования</span><span class="sxs-lookup"><span data-stu-id="67035-119">Requirements</span></span>



| <span data-ttu-id="67035-120">Требование</span><span class="sxs-lookup"><span data-stu-id="67035-120">Requirement</span></span> | <span data-ttu-id="67035-121">Значение</span><span class="sxs-lookup"><span data-stu-id="67035-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="67035-122">Header</span><span class="sxs-lookup"><span data-stu-id="67035-122">Header</span></span><br/> | <dl> <span data-ttu-id="67035-123"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="67035-123"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67035-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67035-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67035-125">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="67035-125">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="67035-126">**Интерфейс Ивмплибрари (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="67035-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





