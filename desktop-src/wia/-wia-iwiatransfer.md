---
description: Интерфейс Ивиатрансфер обеспечивает передачу данных на основе потока.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Интерфейс Ивиатрансфер (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263130"
---
# <a name="iwiatransfer-interface"></a><span data-ttu-id="371d5-103">Интерфейс Ивиатрансфер</span><span class="sxs-lookup"><span data-stu-id="371d5-103">IWiaTransfer interface</span></span>

<span data-ttu-id="371d5-104">Интерфейс **ивиатрансфер** обеспечивает передачу данных на основе потока.</span><span class="sxs-lookup"><span data-stu-id="371d5-104">The **IWiaTransfer** interface provides stream-based transfer of data.</span></span>

## <a name="members"></a><span data-ttu-id="371d5-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="371d5-105">Members</span></span>

<span data-ttu-id="371d5-106">Интерфейс **ивиатрансфер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="371d5-106">The **IWiaTransfer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="371d5-107">**Ивиатрансфер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="371d5-107">**IWiaTransfer** also has these types of members:</span></span>

-   [<span data-ttu-id="371d5-108">Методы</span><span class="sxs-lookup"><span data-stu-id="371d5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="371d5-109">Методы</span><span class="sxs-lookup"><span data-stu-id="371d5-109">Methods</span></span>

<span data-ttu-id="371d5-110">Интерфейс **ивиатрансфер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="371d5-110">The **IWiaTransfer** interface has these methods.</span></span>



| <span data-ttu-id="371d5-111">Метод</span><span class="sxs-lookup"><span data-stu-id="371d5-111">Method</span></span>                                                                 | <span data-ttu-id="371d5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="371d5-112">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="371d5-113">**Отменить**</span><span class="sxs-lookup"><span data-stu-id="371d5-113">**Cancel**</span></span>](-wia-iwiatransfer-cancel.md)                             | <span data-ttu-id="371d5-114">Отменяет текущую операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="371d5-114">Cancels the current transfer operation.</span></span> <br/>                                         |
| [<span data-ttu-id="371d5-115">**Скачать**</span><span class="sxs-lookup"><span data-stu-id="371d5-115">**Download**</span></span>](-wia-iwiatransfer-download.md)                         | <span data-ttu-id="371d5-116">Инициирует загрузку данных в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="371d5-116">Initiates a data download to the caller.</span></span> <br/>                                        |
| [<span data-ttu-id="371d5-117">**\_ \_ Сведения о формате енумвиа**</span><span class="sxs-lookup"><span data-stu-id="371d5-117">**EnumWIA\_FORMAT\_INFO**</span></span>](-wia-iwiatransfer-enumwia-format-info.md) | <span data-ttu-id="371d5-118">Создает перечислитель для форматов перемещения, поддерживаемых устройством WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="371d5-118">Creates an enumerator for the transfer formats that the WIA 2.0 device supports.</span></span><br/> |
| [<span data-ttu-id="371d5-119">**Передать**</span><span class="sxs-lookup"><span data-stu-id="371d5-119">**Upload**</span></span>](-wia-iwiatransfer-upload.md)                             | <span data-ttu-id="371d5-120">Инициирует отправку данных одного элемента от вызывающего.</span><span class="sxs-lookup"><span data-stu-id="371d5-120">Initiates a data upload of a single item from the caller.</span></span> <br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="371d5-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="371d5-121">Remarks</span></span>

<span data-ttu-id="371d5-122">Интерфейс **ивиатрансфер** , как и все интерфейсы модели компонентных объектов (com), наследует методы интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="371d5-122">The **IWiaTransfer** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="371d5-123">Методы IUnknown</span><span class="sxs-lookup"><span data-stu-id="371d5-123">IUnknown Methods</span></span>                                        | <span data-ttu-id="371d5-124">Описание</span><span class="sxs-lookup"><span data-stu-id="371d5-124">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="371d5-125">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="371d5-125">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="371d5-126">Возвращает указатели на поддерживаемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="371d5-126">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="371d5-127">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="371d5-127">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="371d5-128">Увеличивает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="371d5-128">Increments reference count.</span></span>               |
| [<span data-ttu-id="371d5-129">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="371d5-129">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="371d5-130">Уменьшает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="371d5-130">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="371d5-131">Требования</span><span class="sxs-lookup"><span data-stu-id="371d5-131">Requirements</span></span>



| <span data-ttu-id="371d5-132">Требование</span><span class="sxs-lookup"><span data-stu-id="371d5-132">Requirement</span></span> | <span data-ttu-id="371d5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="371d5-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="371d5-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="371d5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="371d5-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="371d5-135">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="371d5-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="371d5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="371d5-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="371d5-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="371d5-138">Header</span><span class="sxs-lookup"><span data-stu-id="371d5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="371d5-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="371d5-139"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="371d5-140">IDL</span><span class="sxs-lookup"><span data-stu-id="371d5-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="371d5-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="371d5-141"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="371d5-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="371d5-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="371d5-143"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="371d5-143"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
