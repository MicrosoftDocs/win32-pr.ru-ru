---
description: Содержит коллекцию объектов, реализующих интерфейс Иконтекстноде и являющихся результатом операции анализа рукописного ввода.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Интерфейс Иконтекстнодес (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711128"
---
# <a name="icontextnodes-interface"></a><span data-ttu-id="18083-103">Интерфейс Иконтекстнодес</span><span class="sxs-lookup"><span data-stu-id="18083-103">IContextNodes interface</span></span>

<span data-ttu-id="18083-104">Содержит коллекцию объектов, реализующих интерфейс [**иконтекстноде**](icontextnode.md) и являющихся результатом операции анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="18083-104">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="18083-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="18083-105">Members</span></span>

<span data-ttu-id="18083-106">Интерфейс **иконтекстнодес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="18083-106">The **IContextNodes** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="18083-107">**Иконтекстнодес** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="18083-107">**IContextNodes** also has these types of members:</span></span>

-   [<span data-ttu-id="18083-108">Методы</span><span class="sxs-lookup"><span data-stu-id="18083-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="18083-109">Методы</span><span class="sxs-lookup"><span data-stu-id="18083-109">Methods</span></span>

<span data-ttu-id="18083-110">Интерфейс **иконтекстнодес** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="18083-110">The **IContextNodes** interface has these methods.</span></span>



| <span data-ttu-id="18083-111">Метод</span><span class="sxs-lookup"><span data-stu-id="18083-111">Method</span></span>                                                       | <span data-ttu-id="18083-112">Описание</span><span class="sxs-lookup"><span data-stu-id="18083-112">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18083-113">**аддконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="18083-113">**AddContextNode**</span></span>](icontextnodes-addcontextnode.md)       | <span data-ttu-id="18083-114">Добавляет объект [**иконтекстноде**](icontextnode.md) в эту коллекцию.</span><span class="sxs-lookup"><span data-stu-id="18083-114">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span> <br/>                                  |
| [<span data-ttu-id="18083-115">**жетконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="18083-115">**GetContextNode**</span></span>](icontextnodes-getcontextnode.md)       | <span data-ttu-id="18083-116">Извлекает объект [**иконтекстноде**](icontextnode.md) по указанному индексу в данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="18083-116">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span> <br/> |
| [<span data-ttu-id="18083-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="18083-117">**GetCount**</span></span>](icontextnodes-getcount.md)                   | <span data-ttu-id="18083-118">Возвращает число объектов [**иконтекстноде**](icontextnode.md) , содержащихся в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="18083-118">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span> <br/>       |
| [<span data-ttu-id="18083-119">**ремовеконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="18083-119">**RemoveContextNode**</span></span>](icontextnodes-removecontextnode.md) | <span data-ttu-id="18083-120">Удаляет объект [**иконтекстноде**](icontextnode.md) из этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="18083-120">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span> <br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="18083-121">Требования</span><span class="sxs-lookup"><span data-stu-id="18083-121">Requirements</span></span>



| <span data-ttu-id="18083-122">Требование</span><span class="sxs-lookup"><span data-stu-id="18083-122">Requirement</span></span> | <span data-ttu-id="18083-123">Значение</span><span class="sxs-lookup"><span data-stu-id="18083-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18083-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18083-124">Minimum supported client</span></span><br/> | <span data-ttu-id="18083-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="18083-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="18083-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18083-126">Minimum supported server</span></span><br/> | <span data-ttu-id="18083-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="18083-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="18083-128">Header</span><span class="sxs-lookup"><span data-stu-id="18083-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="18083-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="18083-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="18083-130">DLL</span><span class="sxs-lookup"><span data-stu-id="18083-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18083-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18083-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="18083-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18083-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18083-133">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="18083-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="18083-134">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="18083-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

