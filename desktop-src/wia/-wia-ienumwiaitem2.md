---
description: Используется приложениями для перечисления объектов IWiaItem2 в текущей папке дерева элементов.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Интерфейс IEnumWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650590"
---
# <a name="ienumwiaitem2-interface"></a><span data-ttu-id="a90ce-103">Интерфейс IEnumWiaItem2</span><span class="sxs-lookup"><span data-stu-id="a90ce-103">IEnumWiaItem2 interface</span></span>

<span data-ttu-id="a90ce-104">Используется приложениями для перечисления объектов [**IWiaItem2**](-wia-iwiaitem2.md) в текущей папке дерева элементов.</span><span class="sxs-lookup"><span data-stu-id="a90ce-104">Used by applications to enumerate [**IWiaItem2**](-wia-iwiaitem2.md) objects in the item tree's current folder.</span></span>

## <a name="members"></a><span data-ttu-id="a90ce-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="a90ce-105">Members</span></span>

<span data-ttu-id="a90ce-106">Интерфейс **IEnumWiaItem2** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a90ce-106">The **IEnumWiaItem2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a90ce-107">**IEnumWiaItem2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a90ce-107">**IEnumWiaItem2** also has these types of members:</span></span>

-   [<span data-ttu-id="a90ce-108">Методы</span><span class="sxs-lookup"><span data-stu-id="a90ce-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a90ce-109">Методы</span><span class="sxs-lookup"><span data-stu-id="a90ce-109">Methods</span></span>

<span data-ttu-id="a90ce-110">Интерфейс **IEnumWiaItem2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a90ce-110">The **IEnumWiaItem2** interface has these methods.</span></span>



| <span data-ttu-id="a90ce-111">Метод</span><span class="sxs-lookup"><span data-stu-id="a90ce-111">Method</span></span>                                          | <span data-ttu-id="a90ce-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a90ce-112">Description</span></span>                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a90ce-113">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="a90ce-113">**Clone**</span></span>](-wia-ienumwiaitem2-clone.md)       | <span data-ttu-id="a90ce-114">Создает дополнительный экземпляр интерфейса **IEnumWiaItem2** и отправляет обратный указатель на него.</span><span class="sxs-lookup"><span data-stu-id="a90ce-114">Creates an additional instance of the **IEnumWiaItem2** interface and sends back a pointer to it.</span></span> <br/>                  |
| [<span data-ttu-id="a90ce-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="a90ce-115">**GetCount**</span></span>](-wia-ienumwiaitem2-getcount.md) | <span data-ttu-id="a90ce-116">Возвращает количество элементов, хранящихся в этом перечислителе.</span><span class="sxs-lookup"><span data-stu-id="a90ce-116">Returns the number of elements stored by this enumerator.</span></span> <br/>                                                          |
| [<span data-ttu-id="a90ce-117">**Далее**</span><span class="sxs-lookup"><span data-stu-id="a90ce-117">**Next**</span></span>](-wia-ienumwiaitem2-next.md)         | <span data-ttu-id="a90ce-118">Заполняет массив указателей на интерфейсы [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="a90ce-118">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="a90ce-119">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="a90ce-119">**Reset**</span></span>](-wia-ienumwiaitem2-reset.md)       | <span data-ttu-id="a90ce-120">Сбрасывает ссылку перечисления на первый объект [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="a90ce-120">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <br/>                          |
| [<span data-ttu-id="a90ce-121">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="a90ce-121">**Skip**</span></span>](-wia-ienumwiaitem2-skip.md)         | <span data-ttu-id="a90ce-122">Пропускает указанное число элементов во время перечисления доступных объектов [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="a90ce-122">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a90ce-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a90ce-123">Requirements</span></span>



| <span data-ttu-id="a90ce-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a90ce-124">Requirement</span></span> | <span data-ttu-id="a90ce-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a90ce-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a90ce-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a90ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a90ce-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a90ce-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a90ce-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a90ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a90ce-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a90ce-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a90ce-130">Header</span><span class="sxs-lookup"><span data-stu-id="a90ce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a90ce-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a90ce-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a90ce-132">IDL</span><span class="sxs-lookup"><span data-stu-id="a90ce-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a90ce-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a90ce-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
