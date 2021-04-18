---
description: Метод OpenView объекта Database возвращает объект представления, представляющий запрос, заданный строкой SQL.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Метод Database. OpenView (Цертвиев. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652255"
---
# <a name="databaseopenview-method"></a><span data-ttu-id="07acd-103">Database. OpenView, метод</span><span class="sxs-lookup"><span data-stu-id="07acd-103">Database.OpenView method</span></span>

<span data-ttu-id="07acd-104">Метод **OpenView** объекта [**Database**](database-object.md) возвращает объект [**представления**](view-object.md) , представляющий запрос, заданный строкой SQL.</span><span class="sxs-lookup"><span data-stu-id="07acd-104">The **OpenView** method of the [**Database**](database-object.md) object returns a [**View**](view-object.md) object that represents the query specified by a SQL string.</span></span>

## <a name="syntax"></a><span data-ttu-id="07acd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07acd-105">Syntax</span></span>


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a><span data-ttu-id="07acd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07acd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07acd-107">*sql*</span><span class="sxs-lookup"><span data-stu-id="07acd-107">*sql*</span></span> 
</dt> <dd>

<span data-ttu-id="07acd-108">Обязательная строка запроса SQL.</span><span class="sxs-lookup"><span data-stu-id="07acd-108">Required SQL query string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07acd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07acd-109">Return value</span></span>

<span data-ttu-id="07acd-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="07acd-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07acd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07acd-111">Remarks</span></span>

<span data-ttu-id="07acd-112">Сведения о синтаксисе SQL, реализованном в установщике, см. в разделе [синтаксис SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="07acd-112">For information about SQL syntax implemented in the installer, see [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="07acd-113">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="07acd-113">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07acd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="07acd-114">Requirements</span></span>



| <span data-ttu-id="07acd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="07acd-115">Requirement</span></span> | <span data-ttu-id="07acd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="07acd-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07acd-117">Версия</span><span class="sxs-lookup"><span data-stu-id="07acd-117">Version</span></span><br/> | <span data-ttu-id="07acd-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="07acd-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="07acd-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="07acd-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="07acd-120">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="07acd-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="07acd-121">Header</span><span class="sxs-lookup"><span data-stu-id="07acd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="07acd-122"><dt>Цертвиев. h</dt></span><span class="sxs-lookup"><span data-stu-id="07acd-122"><dt>Certview.h</dt></span></span> </dl>                                                                                                                                                                   |
| <span data-ttu-id="07acd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="07acd-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="07acd-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07acd-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="07acd-125">IID</span><span class="sxs-lookup"><span data-stu-id="07acd-125">IID</span></span><br/>     | <span data-ttu-id="07acd-126">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="07acd-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="07acd-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07acd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07acd-128">**База данных**</span><span class="sxs-lookup"><span data-stu-id="07acd-128">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="07acd-129">Синтаксис SQL</span><span class="sxs-lookup"><span data-stu-id="07acd-129">SQL Syntax</span></span>](sql-syntax.md)
</dt> </dl>

 

 




