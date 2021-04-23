---
description: Объект Рекордлист представляет собой коллекцию объектов Record. Перед обращением к его свойствам необходимо убедиться, что объект Рекордлист существует и не пуст.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: Объект Рекордлист
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676071"
---
# <a name="recordlist-object"></a><span data-ttu-id="76156-104">Объект Рекордлист</span><span class="sxs-lookup"><span data-stu-id="76156-104">RecordList object</span></span>

<span data-ttu-id="76156-105">Объект **рекордлист** представляет собой коллекцию объектов [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="76156-105">The **RecordList** object is a collection of [**Record**](record-object.md) objects.</span></span> <span data-ttu-id="76156-106">Перед обращением к его свойствам необходимо убедиться, что объект **рекордлист** существует и не пуст.</span><span class="sxs-lookup"><span data-stu-id="76156-106">You must verify that the **RecordList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="76156-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="76156-107">Members</span></span>

<span data-ttu-id="76156-108">Объект **рекордлист** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="76156-108">The **RecordList** object has these types of members:</span></span>

-   [<span data-ttu-id="76156-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="76156-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76156-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="76156-110">Properties</span></span>

<span data-ttu-id="76156-111">Объект **рекордлист** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="76156-111">The **RecordList** object has these properties.</span></span>



| <span data-ttu-id="76156-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="76156-112">Property</span></span>                                     | <span data-ttu-id="76156-113">Описание</span><span class="sxs-lookup"><span data-stu-id="76156-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="76156-114">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="76156-114">**Count**</span></span>](recordlist-count.md)<br/> | <span data-ttu-id="76156-115">Возвращает количество элементов в объекте **рекордлист** .</span><span class="sxs-lookup"><span data-stu-id="76156-115">Returns the number of items in the **RecordList** object.</span></span><br/> |
| [<span data-ttu-id="76156-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="76156-116">**Item**</span></span>](recordlist-item.md)<br/>   | <span data-ttu-id="76156-117">Возвращает запись в коллекции объектов **рекордлист** .</span><span class="sxs-lookup"><span data-stu-id="76156-117">Returns a record in a **RecordList** object collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="76156-118">Требования</span><span class="sxs-lookup"><span data-stu-id="76156-118">Requirements</span></span>



| <span data-ttu-id="76156-119">Требование</span><span class="sxs-lookup"><span data-stu-id="76156-119">Requirement</span></span> | <span data-ttu-id="76156-120">Значение</span><span class="sxs-lookup"><span data-stu-id="76156-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76156-121">Версия</span><span class="sxs-lookup"><span data-stu-id="76156-121">Version</span></span><br/> | <span data-ttu-id="76156-122">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="76156-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="76156-123">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="76156-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="76156-124">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="76156-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="76156-125">DLL</span><span class="sxs-lookup"><span data-stu-id="76156-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="76156-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76156-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="76156-127">IID</span><span class="sxs-lookup"><span data-stu-id="76156-127">IID</span></span><br/>     | <span data-ttu-id="76156-128">IID \_ ирекордлист определен как 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="76156-128">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="76156-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76156-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76156-130">**Записать**</span><span class="sxs-lookup"><span data-stu-id="76156-130">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="76156-131">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="76156-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




