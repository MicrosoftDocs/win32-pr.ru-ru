---
description: Класс коллекции
ms.assetid: 2b2a70ff-2b49-44b2-b506-b0b2cc953ec4
title: Collection - объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Collection
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: cf9c5fc6b01574b930b7b8b74186243d00fa5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345602"
---
# <a name="collection-object"></a><span data-ttu-id="501bc-103">Collection - объект</span><span class="sxs-lookup"><span data-stu-id="501bc-103">Collection object</span></span>

<span data-ttu-id="501bc-104">Класс коллекции</span><span class="sxs-lookup"><span data-stu-id="501bc-104">Collection Class</span></span>

## <a name="members"></a><span data-ttu-id="501bc-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="501bc-105">Members</span></span>

<span data-ttu-id="501bc-106">Объект **коллекции** содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="501bc-106">The **Collection** object has these types of members:</span></span>

-   [<span data-ttu-id="501bc-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="501bc-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="501bc-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="501bc-108">Properties</span></span>

<span data-ttu-id="501bc-109">Объект **коллекции** содержит эти свойства.</span><span class="sxs-lookup"><span data-stu-id="501bc-109">The **Collection** object has these properties.</span></span>



| <span data-ttu-id="501bc-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="501bc-110">Property</span></span>                                           | <span data-ttu-id="501bc-111">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="501bc-111">Access type</span></span>          | <span data-ttu-id="501bc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="501bc-112">Description</span></span>                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="501bc-113">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="501bc-113">**Count**</span></span>](-wia-icollection-count.md)<br/> | <span data-ttu-id="501bc-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="501bc-114">Read-only</span></span><br/> | <span data-ttu-id="501bc-115">Возвращает число элементов в коллекции</span><span class="sxs-lookup"><span data-stu-id="501bc-115">Returns the number of members in the collection</span></span><br/> |
| [<span data-ttu-id="501bc-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="501bc-116">**Item**</span></span>](-wia-icollection-item.md)<br/>   | <span data-ttu-id="501bc-117">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="501bc-117">Read-only</span></span><br/> | <span data-ttu-id="501bc-118">Возвращает указанный элемент в коллекции</span><span class="sxs-lookup"><span data-stu-id="501bc-118">Returns the specified item in the collection</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="501bc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="501bc-119">Remarks</span></span>

### <a name="creationaccess-functions"></a><span data-ttu-id="501bc-120">\\Функции доступа для создания</span><span class="sxs-lookup"><span data-stu-id="501bc-120">Creation\\Access Functions</span></span>

<span data-ttu-id="501bc-121">Чтобы получить ссылку на объект, используйте любой из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="501bc-121">Use any of the following to retrieve a reference to the object:</span></span>



[<span data-ttu-id="501bc-122">**жетитемсфромуи**</span><span class="sxs-lookup"><span data-stu-id="501bc-122">**GetItemsFromUI**</span></span>](-wia-iwiadispatchitem-getitemsfromui.md)

[<span data-ttu-id="501bc-123">**Дети**</span><span class="sxs-lookup"><span data-stu-id="501bc-123">**Children**</span></span>](-wia-iwiadispatchitem-children.md)

[<span data-ttu-id="501bc-124">**Устройства**</span><span class="sxs-lookup"><span data-stu-id="501bc-124">**Devices**</span></span>](-wia-iwia-devices.md)



 

## <a name="requirements"></a><span data-ttu-id="501bc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="501bc-125">Requirements</span></span>



| <span data-ttu-id="501bc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="501bc-126">Requirement</span></span> | <span data-ttu-id="501bc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="501bc-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="501bc-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="501bc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="501bc-129">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="501bc-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="501bc-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="501bc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="501bc-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="501bc-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="501bc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="501bc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="501bc-133"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="501bc-133"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




