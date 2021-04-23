---
description: Содержит коллекцию объектов, реализующих интерфейс Иконтекстлинк.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Интерфейс Иконтекстлинкс (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991163"
---
# <a name="icontextlinks-interface"></a><span data-ttu-id="f7ba7-103">Интерфейс Иконтекстлинкс</span><span class="sxs-lookup"><span data-stu-id="f7ba7-103">IContextLinks interface</span></span>

<span data-ttu-id="f7ba7-104">Содержит коллекцию объектов, реализующих интерфейс [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ba7-104">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="f7ba7-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="f7ba7-105">Members</span></span>

<span data-ttu-id="f7ba7-106">Интерфейс **иконтекстлинкс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f7ba7-106">The **IContextLinks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f7ba7-107">**Иконтекстлинкс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f7ba7-107">**IContextLinks** also has these types of members:</span></span>

-   [<span data-ttu-id="f7ba7-108">Методы</span><span class="sxs-lookup"><span data-stu-id="f7ba7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f7ba7-109">Методы</span><span class="sxs-lookup"><span data-stu-id="f7ba7-109">Methods</span></span>

<span data-ttu-id="f7ba7-110">Интерфейс **иконтекстлинкс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f7ba7-110">The **IContextLinks** interface has these methods.</span></span>



| <span data-ttu-id="f7ba7-111">Метод</span><span class="sxs-lookup"><span data-stu-id="f7ba7-111">Method</span></span>                                                 | <span data-ttu-id="f7ba7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f7ba7-112">Description</span></span>                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7ba7-113">**жетконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="f7ba7-113">**GetContextLink**</span></span>](icontextlinks-getcontextlink.md) | <span data-ttu-id="f7ba7-114">Извлекает [**иконтекстлинк**](icontextlink.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="f7ba7-114">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span><br/>               |
| [<span data-ttu-id="f7ba7-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="f7ba7-115">**GetCount**</span></span>](icontextlinks-getcount.md)             | <span data-ttu-id="f7ba7-116">Возвращает число объектов [**иконтекстлинк**](icontextlink.md) в данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="f7ba7-116">Retrieves the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7ba7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7ba7-117">Remarks</span></span>

<span data-ttu-id="f7ba7-118">Доступ к этому методу обычно осуществляется с помощью метода [**иконтекстноде:: жетконтекстлинкс**](icontextnode-getcontextlinks.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ba7-118">This is usually accessed through the [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7ba7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f7ba7-119">Requirements</span></span>



| <span data-ttu-id="f7ba7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f7ba7-120">Requirement</span></span> | <span data-ttu-id="f7ba7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f7ba7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ba7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7ba7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f7ba7-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f7ba7-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f7ba7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7ba7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f7ba7-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f7ba7-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f7ba7-126">Header</span><span class="sxs-lookup"><span data-stu-id="f7ba7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7ba7-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f7ba7-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f7ba7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f7ba7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7ba7-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7ba7-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f7ba7-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7ba7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ba7-131">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="f7ba7-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="f7ba7-132">**Иконтекстноде:: Аддконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="f7ba7-132">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="f7ba7-133">**Иконтекстноде::D Елетеконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="f7ba7-133">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="f7ba7-134">**Иконтекстноде:: Жетконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="f7ba7-134">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="f7ba7-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="f7ba7-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

