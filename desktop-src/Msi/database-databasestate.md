---
description: Свойство Датабасестате объекта Database доступно только для чтения.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Свойство Database. Датабасестате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651761"
---
# <a name="databasedatabasestate-property"></a><span data-ttu-id="e7481-103">Свойство Database. Датабасестате</span><span class="sxs-lookup"><span data-stu-id="e7481-103">Database.DatabaseState property</span></span>

<span data-ttu-id="e7481-104">Свойство **датабасестате** объекта [**Database**](database-object.md) доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e7481-104">The **DatabaseState** property of the [**Database**](database-object.md) object is a read-only property.</span></span>

<span data-ttu-id="e7481-105">Это свойство возвращает состояние сохраняемости базы данных в виде одного из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="e7481-105">This property returns the persistence state of the database as one of the following parameters.</span></span>



| <span data-ttu-id="e7481-106">Состояние базы данных</span><span class="sxs-lookup"><span data-stu-id="e7481-106">Database state</span></span>        | <span data-ttu-id="e7481-107">Значение</span><span class="sxs-lookup"><span data-stu-id="e7481-107">Value</span></span> | <span data-ttu-id="e7481-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e7481-108">Description</span></span>                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7481-109">мсидатабасестатереад</span><span class="sxs-lookup"><span data-stu-id="e7481-109">msiDatabaseStateRead</span></span>  | <span data-ttu-id="e7481-110">0</span><span class="sxs-lookup"><span data-stu-id="e7481-110">0</span></span>     | <span data-ttu-id="e7481-111">База данных открывается только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e7481-111">Database opens as read-only.</span></span> <span data-ttu-id="e7481-112">Изменения постоянных данных не разрешены, а временные данные не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="e7481-112">Changes to persistent data are not permitted and temporary data is not saved.</span></span> |
| <span data-ttu-id="e7481-113">мсидатабасестатеврите</span><span class="sxs-lookup"><span data-stu-id="e7481-113">msiDatabaseStateWrite</span></span> | <span data-ttu-id="e7481-114">1</span><span class="sxs-lookup"><span data-stu-id="e7481-114">1</span></span>     | <span data-ttu-id="e7481-115">База данных полностью работоспособна для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e7481-115">Database is fully operational for read and write.</span></span>                                                          |



 

<span data-ttu-id="e7481-116">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e7481-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7481-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7481-117">Syntax</span></span>


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a><span data-ttu-id="e7481-118">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e7481-118">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e7481-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e7481-119">Requirements</span></span>



| <span data-ttu-id="e7481-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e7481-120">Requirement</span></span> | <span data-ttu-id="e7481-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e7481-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7481-122">Версия</span><span class="sxs-lookup"><span data-stu-id="e7481-122">Version</span></span><br/> | <span data-ttu-id="e7481-123">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7481-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e7481-124">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7481-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e7481-125">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="e7481-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e7481-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e7481-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="e7481-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7481-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e7481-128">IID</span><span class="sxs-lookup"><span data-stu-id="e7481-128">IID</span></span><br/>     | <span data-ttu-id="e7481-129">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e7481-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




