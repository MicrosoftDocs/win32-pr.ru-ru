---
description: Метод Import объекта базы данных импортирует таблицу базы данных из текстовых архивных файлов, удаляя любую существующую таблицу.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Метод Database. Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665534"
---
# <a name="databaseimport-method"></a><span data-ttu-id="73e87-103">Метод Database. Import</span><span class="sxs-lookup"><span data-stu-id="73e87-103">Database.Import method</span></span>

<span data-ttu-id="73e87-104">Метод **Import** объекта [**базы данных**](database-object.md) импортирует таблицу базы данных из [текстовых архивных файлов](text-archive-files.md), удаляя любую существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="73e87-104">The **Import** method of the [**Database**](database-object.md) object imports a database table from a [text archive files](text-archive-files.md), dropping any existing table.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e87-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73e87-105">Syntax</span></span>


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="73e87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73e87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e87-107">*путь*</span><span class="sxs-lookup"><span data-stu-id="73e87-107">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="73e87-108">Обязательная папка, в которой находится текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="73e87-108">Required folder where the text file is present.</span></span>

</dd> <dt>

<span data-ttu-id="73e87-109">*file*</span><span class="sxs-lookup"><span data-stu-id="73e87-109">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="73e87-110">Обязательное имя импортируемого файла.</span><span class="sxs-lookup"><span data-stu-id="73e87-110">Required name of the file to be imported.</span></span> <span data-ttu-id="73e87-111">Сюда не входит папка, которая должна быть задана в объекте Path.</span><span class="sxs-lookup"><span data-stu-id="73e87-111">This does not include the folder, as that must be set in the path object.</span></span> <span data-ttu-id="73e87-112">Имя таблицы указывается в файле.</span><span class="sxs-lookup"><span data-stu-id="73e87-112">The table name is specified within the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e87-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73e87-113">Return value</span></span>

<span data-ttu-id="73e87-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="73e87-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73e87-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73e87-115">Remarks</span></span>

<span data-ttu-id="73e87-116">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="73e87-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="73e87-117">Требования</span><span class="sxs-lookup"><span data-stu-id="73e87-117">Requirements</span></span>



| <span data-ttu-id="73e87-118">Требование</span><span class="sxs-lookup"><span data-stu-id="73e87-118">Requirement</span></span> | <span data-ttu-id="73e87-119">Значение</span><span class="sxs-lookup"><span data-stu-id="73e87-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e87-120">Версия</span><span class="sxs-lookup"><span data-stu-id="73e87-120">Version</span></span><br/> | <span data-ttu-id="73e87-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="73e87-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="73e87-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="73e87-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="73e87-123">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="73e87-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="73e87-124">DLL</span><span class="sxs-lookup"><span data-stu-id="73e87-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="73e87-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73e87-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="73e87-126">IID</span><span class="sxs-lookup"><span data-stu-id="73e87-126">IID</span></span><br/>     | <span data-ttu-id="73e87-127">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="73e87-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="73e87-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73e87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e87-129">**База данных**</span><span class="sxs-lookup"><span data-stu-id="73e87-129">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="73e87-130">**мсидатабасеимпорт**</span><span class="sxs-lookup"><span data-stu-id="73e87-130">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




