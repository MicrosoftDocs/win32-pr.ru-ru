---
description: Свойство Примарикэйс объекта Database возвращает объект Record, содержащий имя таблицы в поле 0, и имена столбцов (содержащие первичные ключи) в полях, соответствующих их номерам столбцов.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Свойство Database. Примарикэйс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669350"
---
# <a name="databaseprimarykeys-property"></a><span data-ttu-id="05227-103">Свойство Database. Примарикэйс</span><span class="sxs-lookup"><span data-stu-id="05227-103">Database.PrimaryKeys property</span></span>

<span data-ttu-id="05227-104">Свойство **примарикэйс** объекта [**Database**](database-object.md) возвращает объект [**Record**](record-object.md) , содержащий имя таблицы в поле 0, и имена столбцов (содержащие первичные ключи) в полях, соответствующих их номерам столбцов.</span><span class="sxs-lookup"><span data-stu-id="05227-104">The **PrimaryKeys** property of the [**Database**](database-object.md) object returns a [**Record**](record-object.md) object containing the table name in field 0 and the column names (comprising the primary keys) in succeeding fields corresponding to their column numbers.</span></span> <span data-ttu-id="05227-105">Число полей в записи равно числу столбцов первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="05227-105">The field count of the record is the count of primary key columns.</span></span>

<span data-ttu-id="05227-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="05227-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05227-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05227-107">Syntax</span></span>


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a><span data-ttu-id="05227-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="05227-108">Property value</span></span>

<span data-ttu-id="05227-109">Обязательное имя существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="05227-109">Required name of an existing table.</span></span> <span data-ttu-id="05227-110">Если таблица не существует, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="05227-110">An error is generated if the table does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="05227-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05227-111">Remarks</span></span>

<span data-ttu-id="05227-112">Свойство **примарикэйс** не может использоваться с [ \_ таблицей таблиц](-tables-table.md) или [ \_ столбцами](-columns-table.md).</span><span class="sxs-lookup"><span data-stu-id="05227-112">The **PrimaryKeys** property cannot be used with the [\_Tables table](-tables-table.md) or the [\_Columns table](-columns-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05227-113">Требования</span><span class="sxs-lookup"><span data-stu-id="05227-113">Requirements</span></span>



| <span data-ttu-id="05227-114">Требование</span><span class="sxs-lookup"><span data-stu-id="05227-114">Requirement</span></span> | <span data-ttu-id="05227-115">Значение</span><span class="sxs-lookup"><span data-stu-id="05227-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05227-116">Версия</span><span class="sxs-lookup"><span data-stu-id="05227-116">Version</span></span><br/> | <span data-ttu-id="05227-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="05227-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="05227-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="05227-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="05227-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="05227-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="05227-120">DLL</span><span class="sxs-lookup"><span data-stu-id="05227-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="05227-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05227-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="05227-122">IID</span><span class="sxs-lookup"><span data-stu-id="05227-122">IID</span></span><br/>     | <span data-ttu-id="05227-123">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="05227-123">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




