---
description: Интерфейс Ивиасегментатионфилтер определяет подобласти потока изображения и создает отдельные элементы IWiaItem2 для каждого из них.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Интерфейс Ивиасегментатионфилтер (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897442"
---
# <a name="iwiasegmentationfilter-interface"></a><span data-ttu-id="4e0a7-103">Интерфейс Ивиасегментатионфилтер</span><span class="sxs-lookup"><span data-stu-id="4e0a7-103">IWiaSegmentationFilter interface</span></span>

<span data-ttu-id="4e0a7-104">Интерфейс **ивиасегментатионфилтер** определяет подобласти потока изображения и создает отдельные элементы [**IWiaItem2**](-wia-iwiaitem2.md) для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-104">The **IWiaSegmentationFilter** interface detects sub-regions of an image stream and makes separate [**IWiaItem2**](-wia-iwiaitem2.md) items for each.</span></span>

## <a name="members"></a><span data-ttu-id="4e0a7-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="4e0a7-105">Members</span></span>

<span data-ttu-id="4e0a7-106">Интерфейс **ивиасегментатионфилтер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4e0a7-106">The **IWiaSegmentationFilter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4e0a7-107">**Ивиасегментатионфилтер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4e0a7-107">**IWiaSegmentationFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="4e0a7-108">Методы</span><span class="sxs-lookup"><span data-stu-id="4e0a7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4e0a7-109">Методы</span><span class="sxs-lookup"><span data-stu-id="4e0a7-109">Methods</span></span>

<span data-ttu-id="4e0a7-110">Интерфейс **ивиасегментатионфилтер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-110">The **IWiaSegmentationFilter** interface has these methods.</span></span>



| <span data-ttu-id="4e0a7-111">Метод</span><span class="sxs-lookup"><span data-stu-id="4e0a7-111">Method</span></span>                                                             | <span data-ttu-id="4e0a7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4e0a7-112">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e0a7-113">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="4e0a7-113">**DetectRegions**</span></span>](-wia-iwiasegmentationfilter-detectregions.md) | <span data-ttu-id="4e0a7-114">Определяет подобласти изображения, расположенного на планшетном Платен, чтобы каждый из подрегионов можно было получить в отдельный элемент изображения.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-114">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e0a7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e0a7-115">Remarks</span></span>

<span data-ttu-id="4e0a7-116">Приложение должно использовать [**IWiaItem2:: Extension**](-wia-iwiaitem2-getextension.md) для создания нового экземпляра фильтра сегментации.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-116">An application should use [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) to create a new instance of the segmentation filter.</span></span> <span data-ttu-id="4e0a7-117">Приложение обычно вызывает эту функцию перед отображением окна предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-117">An application typically calls this function before displaying its preview window.</span></span>

<span data-ttu-id="4e0a7-118">При реализации этого фильтра используйте [**IWiaItem2:: креатечилдитем**](-wia-iwiaitem2-createchilditem.md) , чтобы создать дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-118">When implementing this filter, use [**IWiaItem2::CreateChildItem**](-wia-iwiaitem2-createchilditem.md) to create the child items.</span></span> <span data-ttu-id="4e0a7-119">Приложение должно передать **\_ \_ \_ значения родительского свойства** в параметр *икреатионфлагс* , чтобы свойства, такие как формат изображения и разрешение, совпадали во вновь созданном дочернем элементе, как в родительском.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-119">The application should pass **COPY\_PARENT\_PROPERTY\_VALUES** to the *ICreationFlags* parameter to ensure that properties such as image format and resolution is the same in the newly created child as in the parent item.</span></span>

<span data-ttu-id="4e0a7-120">Фильтр сегментации должен поддерживать все форматы изображений, поддерживаемые драйвером.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-120">A segmentation filter must support all the image formats that the driver it is used with supports.</span></span> <span data-ttu-id="4e0a7-121">Фильтр, предоставленный корпорацией Майкрософт, поддерживает точечные рисунки (BMP), формат GIF, JPEG, PNG и формат файлов изображений с тегами (TIFF).</span><span class="sxs-lookup"><span data-stu-id="4e0a7-121">The Microsoft provided filter supports bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="4e0a7-122">Фильтр сегментации должен использоваться только для элементов сканера пленки и планшетов.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-122">The segmentation filter should be used only on film and flatbed scanner items.</span></span> <span data-ttu-id="4e0a7-123">Для сканирования на пленке сканер часто поступает с фиксированными кадрами, в которых драйвер создает дочерние элементы, и приложение не должно вызывать фильтр сегментации.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-123">For film scanning, a scanner often comes with fixed frames in which case the driver created the child items and the application should not invoke the segmentation filter.</span></span>

<span data-ttu-id="4e0a7-124">Интерфейс **ивиасегментатионфилтер** , как и все интерфейсы модели компонентных объектов (com), наследует методы интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4e0a7-124">The **IWiaSegmentationFilter** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="4e0a7-125">Методы IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e0a7-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="4e0a7-126">Описание</span><span class="sxs-lookup"><span data-stu-id="4e0a7-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="4e0a7-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="4e0a7-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="4e0a7-128">Возвращает указатели на поддерживаемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="4e0a7-129">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="4e0a7-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="4e0a7-130">Увеличивает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="4e0a7-131">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="4e0a7-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="4e0a7-132">Уменьшает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="4e0a7-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4e0a7-133">Requirements</span></span>



| <span data-ttu-id="4e0a7-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4e0a7-134">Requirement</span></span> | <span data-ttu-id="4e0a7-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4e0a7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0a7-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e0a7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4e0a7-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e0a7-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4e0a7-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e0a7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4e0a7-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e0a7-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4e0a7-140">Header</span><span class="sxs-lookup"><span data-stu-id="4e0a7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e0a7-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e0a7-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e0a7-142">IDL</span><span class="sxs-lookup"><span data-stu-id="4e0a7-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4e0a7-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e0a7-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
