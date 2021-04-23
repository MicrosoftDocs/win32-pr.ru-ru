---
description: Метод Export объекта Database копирует структуру и данные из указанной таблицы в текстовый файл архива.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Метод Database. Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651760"
---
# <a name="databaseexport-method"></a><span data-ttu-id="0a601-103">Метод Database. Export</span><span class="sxs-lookup"><span data-stu-id="0a601-103">Database.Export method</span></span>

<span data-ttu-id="0a601-104">Метод **Export** объекта [**Database**](database-object.md) копирует структуру и данные из указанной таблицы в [текстовый файл архива](text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="0a601-104">The **Export** method of the [**Database**](database-object.md) object copies the structure and data from a specified table to a [text archive file](text-archive-files.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a601-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a601-105">Syntax</span></span>


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="0a601-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a601-107">*table*</span><span class="sxs-lookup"><span data-stu-id="0a601-107">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="0a601-108">Обязательное имя таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="0a601-108">Required name of the database table.</span></span> <span data-ttu-id="0a601-109">С учетом регистра, если используется база данных установщика.</span><span class="sxs-lookup"><span data-stu-id="0a601-109">Case-sensitive if using the installer database.</span></span>

</dd> <dt>

<span data-ttu-id="0a601-110">*путь*</span><span class="sxs-lookup"><span data-stu-id="0a601-110">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="0a601-111">Обязательная строка, которая является путем к папке, в которую помещен текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="0a601-111">Required string that is the path to the folder where the text file is placed.</span></span>

</dd> <dt>

<span data-ttu-id="0a601-112">*file*</span><span class="sxs-lookup"><span data-stu-id="0a601-112">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="0a601-113">Обязательное имя создаваемого файла.</span><span class="sxs-lookup"><span data-stu-id="0a601-113">Required name of the file to be created.</span></span> <span data-ttu-id="0a601-114">Сюда не входит папка, которая должна быть задана в объекте Path.</span><span class="sxs-lookup"><span data-stu-id="0a601-114">This does not include the folder, as that must be set in the path object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a601-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a601-115">Return value</span></span>

<span data-ttu-id="0a601-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0a601-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a601-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a601-117">Remarks</span></span>

<span data-ttu-id="0a601-118">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="0a601-118">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a601-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0a601-119">Requirements</span></span>



| <span data-ttu-id="0a601-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0a601-120">Requirement</span></span> | <span data-ttu-id="0a601-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0a601-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a601-122">Версия</span><span class="sxs-lookup"><span data-stu-id="0a601-122">Version</span></span><br/> | <span data-ttu-id="0a601-123">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0a601-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0a601-124">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0a601-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0a601-125">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="0a601-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0a601-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0a601-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a601-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a601-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0a601-128">IID</span><span class="sxs-lookup"><span data-stu-id="0a601-128">IID</span></span><br/>     | <span data-ttu-id="0a601-129">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0a601-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




