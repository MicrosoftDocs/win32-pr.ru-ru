---
description: Интерфейс IWiaUIExtension2 предоставляет методы, заменяющие стандартный, предоставляемый системой пользовательский интерфейс пользовательским интерфейсом, который предоставляет настраиваемый значок устройства.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Интерфейс IWiaUIExtension2 (Виадевд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991156"
---
# <a name="iwiauiextension2-interface"></a><span data-ttu-id="f23c6-103">Интерфейс IWiaUIExtension2</span><span class="sxs-lookup"><span data-stu-id="f23c6-103">IWiaUIExtension2 interface</span></span>

<span data-ttu-id="f23c6-104">Интерфейс IWiaUIExtension2 предоставляет методы, заменяющие стандартный, предоставляемый системой пользовательский интерфейс пользовательским интерфейсом, который предоставляет настраиваемый значок устройства.</span><span class="sxs-lookup"><span data-stu-id="f23c6-104">The IWiaUIExtension2 interface provides methods that replace the default, system-supplied user interface with a custom user interface, and that provide a custom device icon.</span></span> <span data-ttu-id="f23c6-105">Поставщики устройств могут реализовать этот интерфейс для предоставления настраиваемых пользовательских интерфейсов для своих устройств.</span><span class="sxs-lookup"><span data-stu-id="f23c6-105">Device vendors can implement this interface to provide custom user interfaces for their devices.</span></span>

## <a name="members"></a><span data-ttu-id="f23c6-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="f23c6-106">Members</span></span>

<span data-ttu-id="f23c6-107">Интерфейс **IWiaUIExtension2** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f23c6-107">The **IWiaUIExtension2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f23c6-108">**IWiaUIExtension2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f23c6-108">**IWiaUIExtension2** also has these types of members:</span></span>

-   [<span data-ttu-id="f23c6-109">Методы</span><span class="sxs-lookup"><span data-stu-id="f23c6-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f23c6-110">Методы</span><span class="sxs-lookup"><span data-stu-id="f23c6-110">Methods</span></span>

<span data-ttu-id="f23c6-111">Интерфейс **IWiaUIExtension2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f23c6-111">The **IWiaUIExtension2** interface has these methods.</span></span>



| <span data-ttu-id="f23c6-112">Метод</span><span class="sxs-lookup"><span data-stu-id="f23c6-112">Method</span></span>                                                       | <span data-ttu-id="f23c6-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f23c6-113">Description</span></span>                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f23c6-114">**девицедиалог**</span><span class="sxs-lookup"><span data-stu-id="f23c6-114">**DeviceDialog**</span></span>](-wia-iwiauiextension2-devicedialog.md)   | <span data-ttu-id="f23c6-115">Предоставляет настраиваемый пользовательский интерфейс, который заменяет стандартный системный интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="f23c6-115">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="f23c6-116">**жетдевицеикон**</span><span class="sxs-lookup"><span data-stu-id="f23c6-116">**GetDeviceIcon**</span></span>](-wia-iwiauiextension2-getdeviceicon.md) | <span data-ttu-id="f23c6-117">Возвращает пользовательский значок устройства.</span><span class="sxs-lookup"><span data-stu-id="f23c6-117">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="f23c6-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f23c6-118">Remarks</span></span>



| <span data-ttu-id="f23c6-119">Методы IUnknown</span><span class="sxs-lookup"><span data-stu-id="f23c6-119">IUnknown Methods</span></span>                                        | <span data-ttu-id="f23c6-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f23c6-120">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="f23c6-121">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="f23c6-121">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="f23c6-122">Возвращает указатели на поддерживаемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f23c6-122">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="f23c6-123">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="f23c6-123">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="f23c6-124">Увеличивает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="f23c6-124">Increments reference count.</span></span>               |
| [<span data-ttu-id="f23c6-125">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="f23c6-125">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="f23c6-126">Уменьшает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="f23c6-126">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="f23c6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f23c6-127">Requirements</span></span>



| <span data-ttu-id="f23c6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f23c6-128">Requirement</span></span> | <span data-ttu-id="f23c6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f23c6-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f23c6-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f23c6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f23c6-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f23c6-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f23c6-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f23c6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f23c6-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f23c6-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f23c6-134">Header</span><span class="sxs-lookup"><span data-stu-id="f23c6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f23c6-135"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="f23c6-135"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
