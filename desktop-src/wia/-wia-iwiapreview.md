---
description: Интерфейс Ивиапревиев кэширует нефильтрованные изображения внутренним образом и передает их через фильтры обработки изображений.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Интерфейс Ивиапревиев (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5e1c01daae4e86fa18c087b67bf902daaf6f8793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263134"
---
# <a name="iwiapreview-interface"></a><span data-ttu-id="7ff91-103">Интерфейс Ивиапревиев</span><span class="sxs-lookup"><span data-stu-id="7ff91-103">IWiaPreview interface</span></span>

<span data-ttu-id="7ff91-104">Интерфейс **ивиапревиев** кэширует нефильтрованные изображения внутренним образом и передает их через фильтры обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="7ff91-104">The **IWiaPreview** interface caches unfiltered images internally and passes them through image processing filters.</span></span>

## <a name="members"></a><span data-ttu-id="7ff91-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="7ff91-105">Members</span></span>

<span data-ttu-id="7ff91-106">Интерфейс **ивиапревиев** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7ff91-106">The **IWiaPreview** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7ff91-107">**Ивиапревиев** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7ff91-107">**IWiaPreview** also has these types of members:</span></span>

-   [<span data-ttu-id="7ff91-108">Методы</span><span class="sxs-lookup"><span data-stu-id="7ff91-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7ff91-109">Методы</span><span class="sxs-lookup"><span data-stu-id="7ff91-109">Methods</span></span>

<span data-ttu-id="7ff91-110">Интерфейс **ивиапревиев** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7ff91-110">The **IWiaPreview** interface has these methods.</span></span>



| <span data-ttu-id="7ff91-111">Метод</span><span class="sxs-lookup"><span data-stu-id="7ff91-111">Method</span></span>                                                  | <span data-ttu-id="7ff91-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7ff91-112">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ff91-113">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="7ff91-113">**Clear**</span></span>](-wia-iwiapreview-clear.md)                 | <span data-ttu-id="7ff91-114">Освобождает нефильтрованное изображение, кэшированное методом [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff91-114">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="7ff91-115">Он также освобождает фильтр обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="7ff91-115">It also releases the image processing filter.</span></span> <br/>          |
| [<span data-ttu-id="7ff91-116">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="7ff91-116">**DetectRegions**</span></span>](-wia-iwiapreview-detectregions.md) | <span data-ttu-id="7ff91-117">Вызывает фильтр сегментации драйвера и передает в фильтр нефильтрованное изображение, кэшированное методом [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff91-117">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span> <br/> |
| [<span data-ttu-id="7ff91-118">**жетневпревиев**</span><span class="sxs-lookup"><span data-stu-id="7ff91-118">**GetNewPreview**</span></span>](-wia-iwiapreview-getnewpreview.md) | <span data-ttu-id="7ff91-119">Внутренне кэширует нефильтрованное изображение, возвращенное драйвером.</span><span class="sxs-lookup"><span data-stu-id="7ff91-119">Caches internally the unfiltered image returned from the driver.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="7ff91-120">**упдатепревиев**</span><span class="sxs-lookup"><span data-stu-id="7ff91-120">**UpdatePreview**</span></span>](-wia-iwiapreview-updatepreview.md) | <span data-ttu-id="7ff91-121">Возвращает нефильтрованное изображение, кэшированное методом [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff91-121">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="7ff91-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ff91-122">Remarks</span></span>

<span data-ttu-id="7ff91-123">Этот фильтр вызывается автоматически методом [**ивиатрансфер::D гружать**](-wia-iwiatransfer-download.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff91-123">This filter is called automatically by the [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) method.</span></span>

<span data-ttu-id="7ff91-124">Интерфейс **ивиапревиев** , как и все интерфейсы модели компонентных объектов (com), наследует методы интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7ff91-124">The **IWiaPreview** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="7ff91-125">Методы IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ff91-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="7ff91-126">Описание</span><span class="sxs-lookup"><span data-stu-id="7ff91-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="7ff91-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="7ff91-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="7ff91-128">Возвращает указатели на поддерживаемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="7ff91-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="7ff91-129">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="7ff91-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="7ff91-130">Увеличивает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="7ff91-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="7ff91-131">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="7ff91-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="7ff91-132">Уменьшает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="7ff91-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="7ff91-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7ff91-133">Requirements</span></span>



| <span data-ttu-id="7ff91-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7ff91-134">Requirement</span></span> | <span data-ttu-id="7ff91-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7ff91-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff91-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ff91-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff91-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ff91-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7ff91-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ff91-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff91-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ff91-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7ff91-140">Header</span><span class="sxs-lookup"><span data-stu-id="7ff91-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ff91-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ff91-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ff91-142">IDL</span><span class="sxs-lookup"><span data-stu-id="7ff91-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ff91-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ff91-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
