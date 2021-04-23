---
description: Метод Commit объекта Database завершает постоянную форму базы данных.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652134"
---
# <a name="databasecommit-method"></a><span data-ttu-id="ff45b-103">Database. Commit, метод</span><span class="sxs-lookup"><span data-stu-id="ff45b-103">Database.Commit method</span></span>

<span data-ttu-id="ff45b-104">Метод **commit** объекта [**Database**](database-object.md) завершает постоянную форму базы данных.</span><span class="sxs-lookup"><span data-stu-id="ff45b-104">The **Commit** method of the [**Database**](database-object.md) object finalizes the persistent form of the database.</span></span> <span data-ttu-id="ff45b-105">Все постоянные данные записываются в базу данных, доступную для записи, а временные столбцы или строки не записываются.</span><span class="sxs-lookup"><span data-stu-id="ff45b-105">All persistent data is written to the writeable database, and no temporary columns or rows are written.</span></span> <span data-ttu-id="ff45b-106">Этот метод не влияет на базу данных, открытую только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ff45b-106">This method has no effect on a database opened as read-only.</span></span> <span data-ttu-id="ff45b-107">Этот метод может вызываться несколько раз для сохранения текущего состояния таблиц, загруженных в память.</span><span class="sxs-lookup"><span data-stu-id="ff45b-107">This method can be called multiple times to save the current state of tables loaded into memory.</span></span> <span data-ttu-id="ff45b-108">Когда база данных закрывается, выполняется откат всех изменений, сделанных после последней **фиксации** .</span><span class="sxs-lookup"><span data-stu-id="ff45b-108">When the database is finally closed, any changes made subsequent to the last **Commit** are rolled back.</span></span> <span data-ttu-id="ff45b-109">Этот метод обычно вызывается перед завершением работы, когда все изменения базы данных были завершены.</span><span class="sxs-lookup"><span data-stu-id="ff45b-109">This method is normally called prior to shutdown when all database changes have been finalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff45b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff45b-110">Syntax</span></span>


```JScript
Database.Commit()
```



## <a name="parameters"></a><span data-ttu-id="ff45b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff45b-111">Parameters</span></span>

<span data-ttu-id="ff45b-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ff45b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff45b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff45b-113">Return value</span></span>

<span data-ttu-id="ff45b-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ff45b-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff45b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff45b-115">Remarks</span></span>

<span data-ttu-id="ff45b-116">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="ff45b-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff45b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ff45b-117">Requirements</span></span>



| <span data-ttu-id="ff45b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ff45b-118">Requirement</span></span> | <span data-ttu-id="ff45b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ff45b-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff45b-120">Версия</span><span class="sxs-lookup"><span data-stu-id="ff45b-120">Version</span></span><br/> | <span data-ttu-id="ff45b-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ff45b-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ff45b-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ff45b-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ff45b-123">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff45b-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ff45b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ff45b-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="ff45b-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff45b-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ff45b-126">IID</span><span class="sxs-lookup"><span data-stu-id="ff45b-126">IID</span></span><br/>     | <span data-ttu-id="ff45b-127">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ff45b-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




