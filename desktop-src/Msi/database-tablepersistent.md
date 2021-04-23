---
description: Свойство Таблеперсистент объекта Database возвращает состояние сохраняемости таблицы как один из следующих параметров.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Свойство Database. Таблеперсистент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669349"
---
# <a name="databasetablepersistent-property"></a><span data-ttu-id="541f1-103">Свойство Database. Таблеперсистент</span><span class="sxs-lookup"><span data-stu-id="541f1-103">Database.TablePersistent property</span></span>

<span data-ttu-id="541f1-104">Свойство **таблеперсистент** объекта [**Database**](database-object.md) возвращает состояние сохраняемости таблицы как один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="541f1-104">The **TablePersistent** property of the [**Database**](database-object.md) object returns the persistence state of the table as one of the following parameters.</span></span>



| <span data-ttu-id="541f1-105">Состояние таблицы</span><span class="sxs-lookup"><span data-stu-id="541f1-105">Table state</span></span>               | <span data-ttu-id="541f1-106">Значение</span><span class="sxs-lookup"><span data-stu-id="541f1-106">Value</span></span> | <span data-ttu-id="541f1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="541f1-107">Description</span></span>                    |
|---------------------------|-------|--------------------------------|
| <span data-ttu-id="541f1-108">мсиевалуатекондитионфалсе</span><span class="sxs-lookup"><span data-stu-id="541f1-108">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="541f1-109">0</span><span class="sxs-lookup"><span data-stu-id="541f1-109">0</span></span>     | <span data-ttu-id="541f1-110">Таблица является временной.</span><span class="sxs-lookup"><span data-stu-id="541f1-110">Table is temporary.</span></span>            |
| <span data-ttu-id="541f1-111">мсиевалуатекондитионтруе</span><span class="sxs-lookup"><span data-stu-id="541f1-111">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="541f1-112">1</span><span class="sxs-lookup"><span data-stu-id="541f1-112">1</span></span>     | <span data-ttu-id="541f1-113">Таблица является постоянной.</span><span class="sxs-lookup"><span data-stu-id="541f1-113">Table is persistent.</span></span>           |
| <span data-ttu-id="541f1-114">мсиевалуатекондитионноне</span><span class="sxs-lookup"><span data-stu-id="541f1-114">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="541f1-115">2</span><span class="sxs-lookup"><span data-stu-id="541f1-115">2</span></span>     | <span data-ttu-id="541f1-116">Таблица отсутствует в базе данных.</span><span class="sxs-lookup"><span data-stu-id="541f1-116">Table is not in the database.</span></span>  |
| <span data-ttu-id="541f1-117">мсиевалуатекондитионеррор</span><span class="sxs-lookup"><span data-stu-id="541f1-117">msiEvaluateConditionError</span></span> | <span data-ttu-id="541f1-118">3</span><span class="sxs-lookup"><span data-stu-id="541f1-118">3</span></span>     | <span data-ttu-id="541f1-119">Имя таблицы недопустимо или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="541f1-119">Invalid or missing table name.</span></span> |



 

<span data-ttu-id="541f1-120">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="541f1-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="541f1-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="541f1-121">Syntax</span></span>


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a><span data-ttu-id="541f1-122">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="541f1-122">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="541f1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="541f1-123">Requirements</span></span>



| <span data-ttu-id="541f1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="541f1-124">Requirement</span></span> | <span data-ttu-id="541f1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="541f1-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="541f1-126">Версия</span><span class="sxs-lookup"><span data-stu-id="541f1-126">Version</span></span><br/> | <span data-ttu-id="541f1-127">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="541f1-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="541f1-128">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="541f1-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="541f1-129">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="541f1-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="541f1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="541f1-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="541f1-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="541f1-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="541f1-132">IID</span><span class="sxs-lookup"><span data-stu-id="541f1-132">IID</span></span><br/>     | <span data-ttu-id="541f1-133">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="541f1-133">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




