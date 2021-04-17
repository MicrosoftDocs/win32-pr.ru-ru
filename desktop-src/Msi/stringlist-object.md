---
description: Объект Стринглист представляет собой коллекцию строк. Клиент должен убедиться, что объект Стринглист существует и не пуст, прежде чем ссылаться на его свойства.
ms.assetid: 7021320a-d01a-43e8-90a5-6105a11a4613
title: Объект Стринглист
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6493b9e1723d46ce290c7472bbcee7eb9ec34725
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675497"
---
# <a name="stringlist-object"></a><span data-ttu-id="2540d-104">Объект Стринглист</span><span class="sxs-lookup"><span data-stu-id="2540d-104">StringList object</span></span>

<span data-ttu-id="2540d-105">Объект **стринглист** представляет собой коллекцию строк.</span><span class="sxs-lookup"><span data-stu-id="2540d-105">The **StringList** object is a collection of strings.</span></span> <span data-ttu-id="2540d-106">Клиент должен убедиться, что объект **стринглист** существует и не пуст, прежде чем ссылаться на его свойства.</span><span class="sxs-lookup"><span data-stu-id="2540d-106">The client must verify that the **StringList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="2540d-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="2540d-107">Members</span></span>

<span data-ttu-id="2540d-108">Объект **стринглист** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2540d-108">The **StringList** object has these types of members:</span></span>

-   [<span data-ttu-id="2540d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="2540d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2540d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2540d-110">Properties</span></span>

<span data-ttu-id="2540d-111">Объект **стринглист** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2540d-111">The **StringList** object has these properties.</span></span>



| <span data-ttu-id="2540d-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="2540d-112">Property</span></span>                                     | <span data-ttu-id="2540d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2540d-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="2540d-114">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="2540d-114">**Count**</span></span>](stringlist-count.md)<br/> | <span data-ttu-id="2540d-115">Возвращает количество элементов в объекте **стринглист** .</span><span class="sxs-lookup"><span data-stu-id="2540d-115">Returns the number of items in the **StringList** object.</span></span><br/> |
| [<span data-ttu-id="2540d-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2540d-116">**Item**</span></span>](stringlist-item.md)<br/>   | <span data-ttu-id="2540d-117">Возвращает строку в коллекции объектов **стринглист** .</span><span class="sxs-lookup"><span data-stu-id="2540d-117">Returns a string in the **StringList** object collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2540d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2540d-118">Requirements</span></span>



| <span data-ttu-id="2540d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2540d-119">Requirement</span></span> | <span data-ttu-id="2540d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2540d-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2540d-121">Версия</span><span class="sxs-lookup"><span data-stu-id="2540d-121">Version</span></span><br/> | <span data-ttu-id="2540d-122">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2540d-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2540d-123">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2540d-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2540d-124">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="2540d-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2540d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2540d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2540d-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2540d-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2540d-127">IID</span><span class="sxs-lookup"><span data-stu-id="2540d-127">IID</span></span><br/>     | <span data-ttu-id="2540d-128">IID \_ истринглист определен как 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2540d-128">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="2540d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2540d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2540d-130">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="2540d-130">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




