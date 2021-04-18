---
description: Интерфейс Ивиауиекстенсион предоставляет методы, которые заменяют системный интерфейс по умолчанию, предоставляют пользовательский логотип точечного рисунка устройства и предоставляют пользовательский значок устройства.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Интерфейс Ивиауиекстенсион (Виадевд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719344"
---
# <a name="iwiauiextension-interface"></a><span data-ttu-id="2679e-103">Интерфейс Ивиауиекстенсион</span><span class="sxs-lookup"><span data-stu-id="2679e-103">IWiaUIExtension interface</span></span>

<span data-ttu-id="2679e-104">Интерфейс **ивиауиекстенсион** предоставляет методы, которые заменяют системный интерфейс по умолчанию, предоставляют пользовательский логотип точечного рисунка устройства и предоставляют пользовательский значок устройства.</span><span class="sxs-lookup"><span data-stu-id="2679e-104">The **IWiaUIExtension** interface provides methods that replace the default system user interface, provide a custom device bitmap logo, and provide a custom device icon.</span></span>

## <a name="members"></a><span data-ttu-id="2679e-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="2679e-105">Members</span></span>

<span data-ttu-id="2679e-106">Интерфейс **ивиауиекстенсион** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2679e-106">The **IWiaUIExtension** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2679e-107">**Ивиауиекстенсион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2679e-107">**IWiaUIExtension** also has these types of members:</span></span>

-   [<span data-ttu-id="2679e-108">Методы</span><span class="sxs-lookup"><span data-stu-id="2679e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2679e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="2679e-109">Methods</span></span>

<span data-ttu-id="2679e-110">Интерфейс **ивиауиекстенсион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2679e-110">The **IWiaUIExtension** interface has these methods.</span></span>



| <span data-ttu-id="2679e-111">Метод</span><span class="sxs-lookup"><span data-stu-id="2679e-111">Method</span></span>                                                                  | <span data-ttu-id="2679e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2679e-112">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2679e-113">**девицедиалог**</span><span class="sxs-lookup"><span data-stu-id="2679e-113">**DeviceDialog**</span></span>](-wia-iwiauiextension-devicedialog.md)               | <span data-ttu-id="2679e-114">Предоставляет настраиваемый пользовательский интерфейс, который заменяет стандартный системный интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="2679e-114">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="2679e-115">**жетдевицебитмаплого**</span><span class="sxs-lookup"><span data-stu-id="2679e-115">**GetDeviceBitmapLogo**</span></span>](-wia-iwiauiextension-getdevicebitmaplogo.md) | <span data-ttu-id="2679e-116">Возвращает пользовательский логотип точечного рисунка для устройства.</span><span class="sxs-lookup"><span data-stu-id="2679e-116">Gets a custom bitmap logo for the device.</span></span><br/>                                         |
| [<span data-ttu-id="2679e-117">**жетдевицеикон**</span><span class="sxs-lookup"><span data-stu-id="2679e-117">**GetDeviceIcon**</span></span>](-wia-iwiauiextension-getdeviceicon.md)             | <span data-ttu-id="2679e-118">Возвращает пользовательский значок устройства.</span><span class="sxs-lookup"><span data-stu-id="2679e-118">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="2679e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2679e-119">Remarks</span></span>



| <span data-ttu-id="2679e-120">Методы IUnknown</span><span class="sxs-lookup"><span data-stu-id="2679e-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="2679e-121">Описание</span><span class="sxs-lookup"><span data-stu-id="2679e-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="2679e-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="2679e-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="2679e-123">Возвращает указатели на поддерживаемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2679e-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="2679e-124">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="2679e-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="2679e-125">Увеличивает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="2679e-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="2679e-126">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="2679e-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="2679e-127">Уменьшает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="2679e-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="2679e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="2679e-128">Requirements</span></span>



| <span data-ttu-id="2679e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="2679e-129">Requirement</span></span> | <span data-ttu-id="2679e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2679e-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2679e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2679e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2679e-132">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2679e-132">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2679e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2679e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2679e-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2679e-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2679e-135">Header</span><span class="sxs-lookup"><span data-stu-id="2679e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2679e-136"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="2679e-136"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
