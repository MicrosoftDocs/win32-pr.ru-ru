---
description: Интерфейс Ивиатрансферкаллбакк принимает обратные вызовы во время обмена данными.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Интерфейс Ивиатрансферкаллбакк (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145391"
---
# <a name="iwiatransfercallback-interface"></a><span data-ttu-id="3e772-103">Интерфейс Ивиатрансферкаллбакк</span><span class="sxs-lookup"><span data-stu-id="3e772-103">IWiaTransferCallback interface</span></span>

<span data-ttu-id="3e772-104">Интерфейс **ивиатрансферкаллбакк** принимает обратные вызовы во время обмена данными.</span><span class="sxs-lookup"><span data-stu-id="3e772-104">The **IWiaTransferCallback** interface receives callbacks during a data transfer.</span></span>

## <a name="members"></a><span data-ttu-id="3e772-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="3e772-105">Members</span></span>

<span data-ttu-id="3e772-106">Интерфейс **ивиатрансферкаллбакк** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3e772-106">The **IWiaTransferCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3e772-107">**Ивиатрансферкаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3e772-107">**IWiaTransferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="3e772-108">Методы</span><span class="sxs-lookup"><span data-stu-id="3e772-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e772-109">Методы</span><span class="sxs-lookup"><span data-stu-id="3e772-109">Methods</span></span>

<span data-ttu-id="3e772-110">Интерфейс **ивиатрансферкаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3e772-110">The **IWiaTransferCallback** interface has these methods.</span></span>



| <span data-ttu-id="3e772-111">Метод</span><span class="sxs-lookup"><span data-stu-id="3e772-111">Method</span></span>                                                                 | <span data-ttu-id="3e772-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3e772-112">Description</span></span>                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="3e772-113">**жетнекстстреам**</span><span class="sxs-lookup"><span data-stu-id="3e772-113">**GetNextStream**</span></span>](-wia-iwiatransfercallback-getnextstream.md)       | <span data-ttu-id="3e772-114">Возвращает новый поток для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="3e772-114">Gets a new stream for the specified item.</span></span> <br/>                    |
| [<span data-ttu-id="3e772-115">**трансферкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="3e772-115">**TransferCallback**</span></span>](-wia-iwiatransfercallback-transfercallback.md) | <span data-ttu-id="3e772-116">Предоставляет ход выполнения и другие уведомления во время перемещения.</span><span class="sxs-lookup"><span data-stu-id="3e772-116">Provides progress and other notifications during a transfer.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e772-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e772-117">Remarks</span></span>

<span data-ttu-id="3e772-118">Разработчики фильтра обработки изображений должны реализовать этот интерфейс и интерфейс [**ивиаимажефилтер**](-wia-iwiaimagefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="3e772-118">Image processing filter developers should implement this interface and the [**IWiaImageFilter**](-wia-iwiaimagefilter.md) interface.</span></span>

<span data-ttu-id="3e772-119">Интерфейс **ивиатрансферкаллбакк** , как и все интерфейсы модели компонентных объектов (com), наследует методы интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3e772-119">The **IWiaTransferCallback** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="3e772-120">Методы IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e772-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="3e772-121">Описание</span><span class="sxs-lookup"><span data-stu-id="3e772-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3e772-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="3e772-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="3e772-123">Возвращает указатели на поддерживаемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="3e772-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="3e772-124">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="3e772-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="3e772-125">Увеличивает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="3e772-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="3e772-126">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="3e772-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="3e772-127">Уменьшает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="3e772-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="3e772-128">Требования</span><span class="sxs-lookup"><span data-stu-id="3e772-128">Requirements</span></span>



| <span data-ttu-id="3e772-129">Требование</span><span class="sxs-lookup"><span data-stu-id="3e772-129">Requirement</span></span> | <span data-ttu-id="3e772-130">Значение</span><span class="sxs-lookup"><span data-stu-id="3e772-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e772-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e772-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3e772-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e772-132">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3e772-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e772-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3e772-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e772-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3e772-135">Header</span><span class="sxs-lookup"><span data-stu-id="3e772-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e772-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e772-136"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="3e772-137">IDL</span><span class="sxs-lookup"><span data-stu-id="3e772-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e772-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e772-138"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="3e772-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e772-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e772-140"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e772-140"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
