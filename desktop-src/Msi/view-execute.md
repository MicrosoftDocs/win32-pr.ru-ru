---
description: Метод Execute объекта View использует маркер вопросительного знака для представления параметров в инструкции SQL. Дополнительные сведения см. в разделе синтаксис SQL. Значения этих параметров передаются в качестве соответствующих полей записи параметра.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exeметод милые
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651635"
---
# <a name="viewexecute-method"></a><span data-ttu-id="5413d-105">View.Exeметод милые</span><span class="sxs-lookup"><span data-stu-id="5413d-105">View.Execute method</span></span>

<span data-ttu-id="5413d-106">Метод **EXECUTE** объекта [**View**](view-object.md) использует маркер вопросительного знака для представления параметров в инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="5413d-106">The **Execute** method of the [**View**](view-object.md) object uses the question mark token to represent parameters in an SQL statement.</span></span> <span data-ttu-id="5413d-107">Дополнительные сведения см. в разделе [синтаксис SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="5413d-107">For more information, see [SQL Syntax](sql-syntax.md).</span></span> <span data-ttu-id="5413d-108">Значения этих параметров передаются в качестве соответствующих полей записи параметра.</span><span class="sxs-lookup"><span data-stu-id="5413d-108">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5413d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5413d-109">Syntax</span></span>


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="5413d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5413d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5413d-111">*record*</span><span class="sxs-lookup"><span data-stu-id="5413d-111">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="5413d-112">Необязательные объекты [**Record**](record-object.md) , которые содержат значения, заменяющие маркеры параметров (?) в SQL-запросе.</span><span class="sxs-lookup"><span data-stu-id="5413d-112">Optional [**Record**](record-object.md) objects that contains the values that replace the parameter tokens (?) in the SQL query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5413d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5413d-113">Return value</span></span>

<span data-ttu-id="5413d-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5413d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5413d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5413d-115">Remarks</span></span>

<span data-ttu-id="5413d-116">Этот метод должен вызываться перед вызовом метода [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="5413d-116">This method must be called before any calls to the [**Fetch**](view-fetch.md) method.</span></span>

<span data-ttu-id="5413d-117">Если SQL-запрос указывает значения с маркерами параметров (?), необходимо указать запись, содержащую все замещающие значения, которые должны находиться в том же порядке и в том же типе данных, что и маркеры параметров.</span><span class="sxs-lookup"><span data-stu-id="5413d-117">If the SQL query specifies values with parameter markers (?), a record must be supplied that contains all of the replacement values, which must be in the same order and of the same data type as the parameter markers.</span></span> <span data-ttu-id="5413d-118">Если этот метод используется с запросами INSERT и UPDATE, маркеры вопросительного знака должны предшествовать всем непараметризованным значениям.</span><span class="sxs-lookup"><span data-stu-id="5413d-118">When this method is used with INSERT and UPDATE queries, the question mark tokens must precede all the non-parameterized values.</span></span>

<span data-ttu-id="5413d-119">Например, эти запросы являются допустимыми:</span><span class="sxs-lookup"><span data-stu-id="5413d-119">For example, these queries are valid:</span></span>

<span data-ttu-id="5413d-120">Обновление {Table-List} SET {Column} =?</span><span class="sxs-lookup"><span data-stu-id="5413d-120">UPDATE {table-list} SET {column}= ?</span></span> <span data-ttu-id="5413d-121">, {Column} = {константа}</span><span class="sxs-lookup"><span data-stu-id="5413d-121">, {column}= {constant}</span></span>

<span data-ttu-id="5413d-122">ВСТАВИТЬ в {Table} ({Column-List}) значения (?, {Constant-List})</span><span class="sxs-lookup"><span data-stu-id="5413d-122">INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})</span></span>

<span data-ttu-id="5413d-123">Однако эти запросы являются недопустимыми:</span><span class="sxs-lookup"><span data-stu-id="5413d-123">However these queries are invalid:</span></span>

<span data-ttu-id="5413d-124">Обновление {Table-List} SET {Column} = {константа}, {Column} =?</span><span class="sxs-lookup"><span data-stu-id="5413d-124">UPDATE {table-list} SET {column}= {constant}, {column}=?</span></span>

<span data-ttu-id="5413d-125">ВСТАВИТЬ в {Table} ({Column-List}) значения ({Constant-List},?</span><span class="sxs-lookup"><span data-stu-id="5413d-125">INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ?</span></span> <span data-ttu-id="5413d-126">)</span><span class="sxs-lookup"><span data-stu-id="5413d-126">)</span></span>

<span data-ttu-id="5413d-127">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="5413d-127">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5413d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="5413d-128">Requirements</span></span>



| <span data-ttu-id="5413d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="5413d-129">Requirement</span></span> | <span data-ttu-id="5413d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5413d-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5413d-131">Версия</span><span class="sxs-lookup"><span data-stu-id="5413d-131">Version</span></span><br/> | <span data-ttu-id="5413d-132">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5413d-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5413d-133">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5413d-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5413d-134">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="5413d-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5413d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5413d-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="5413d-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5413d-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5413d-137">IID</span><span class="sxs-lookup"><span data-stu-id="5413d-137">IID</span></span><br/>     | <span data-ttu-id="5413d-138">IID \_ IView определен как 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5413d-138">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




