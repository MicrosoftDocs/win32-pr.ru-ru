---
description: Метод GenerateTransform объекта Database создает преобразование, которое при применении к базе данных объектов приводит к созданию справочной базы данных. Преобразование хранится в объекте хранилища.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Database. GenerateTransform, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651801"
---
# <a name="databasegeneratetransform-method"></a><span data-ttu-id="6f8d8-104">Database. GenerateTransform, метод</span><span class="sxs-lookup"><span data-stu-id="6f8d8-104">Database.GenerateTransform method</span></span>

<span data-ttu-id="6f8d8-105">Метод **GenerateTransform** объекта [**Database**](database-object.md) создает [*Преобразование*](t-gly.md) , которое при применении к базе данных объектов приводит к созданию справочной базы данных.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-105">The **GenerateTransform** method of the [**Database**](database-object.md) object creates a [*transform*](t-gly.md) that, when applied to the object database, results in the reference database.</span></span> <span data-ttu-id="6f8d8-106">Преобразование хранится в объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-106">The transform is stored in the storage object.</span></span>

<span data-ttu-id="6f8d8-107">Если преобразование должно быть применено во время установки, необходимо использовать метод [**креатетрансформсуммаринфо**](database-createtransformsummaryinfo.md) для заполнения сводного информационного потока.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-107">If the transform is to be applied during an installation you must use the [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) method to populate the summary information stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f8d8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f8d8-108">Syntax</span></span>


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a><span data-ttu-id="6f8d8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f8d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f8d8-110">*reference*</span><span class="sxs-lookup"><span data-stu-id="6f8d8-110">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="6f8d8-111">Требуемая база данных, не включающая изменения.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-111">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="6f8d8-112">*storage*</span><span class="sxs-lookup"><span data-stu-id="6f8d8-112">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="6f8d8-113">Имя созданного файла преобразования.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-113">The name of the generated transform file.</span></span> <span data-ttu-id="6f8d8-114">Это необязательно.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-114">This is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f8d8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f8d8-115">Return value</span></span>

<span data-ttu-id="6f8d8-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f8d8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f8d8-117">Remarks</span></span>

<span data-ttu-id="6f8d8-118">Преобразование может добавлять непервичные ключевые столбцы в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-118">A transform can add non-primary key columns to the end of a table.</span></span> <span data-ttu-id="6f8d8-119">Невозможно создать преобразование, которое добавляет столбцы первичного ключа в таблицу.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-119">A transform cannot be created that adds primary key columns to a table.</span></span> <span data-ttu-id="6f8d8-120">Невозможно создать преобразование, которое изменяет порядок, имена или определения столбцов.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-120">A transform cannot be created that changes the order, names, or definitions of columns.</span></span>

<span data-ttu-id="6f8d8-121">Этот метод возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-121">This method returns a Boolean value.</span></span> <span data-ttu-id="6f8d8-122">Он возвращает значение TRUE, если создается преобразование.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-122">It returns TRUE if a transform is generated.</span></span> <span data-ttu-id="6f8d8-123">Он возвращает значение FALSE, если преобразование не создается из-за отсутствия различий между двумя базами данных.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-123">It returns FALSE if a transform is not generated because there are no differences between the two databases.</span></span> <span data-ttu-id="6f8d8-124">Если метод завершается с ошибкой, выдается ошибка.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-124">If the method fails, it generates an error.</span></span>

<span data-ttu-id="6f8d8-125">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="6f8d8-125">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f8d8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6f8d8-126">Requirements</span></span>



| <span data-ttu-id="6f8d8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6f8d8-127">Requirement</span></span> | <span data-ttu-id="6f8d8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6f8d8-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8d8-129">Версия</span><span class="sxs-lookup"><span data-stu-id="6f8d8-129">Version</span></span><br/> | <span data-ttu-id="6f8d8-130">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6f8d8-131">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f8d8-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6f8d8-132">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f8d8-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6f8d8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6f8d8-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="6f8d8-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f8d8-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6f8d8-135">IID</span><span class="sxs-lookup"><span data-stu-id="6f8d8-135">IID</span></span><br/>     | <span data-ttu-id="6f8d8-136">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6f8d8-136">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="6f8d8-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f8d8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f8d8-138">**База данных**</span><span class="sxs-lookup"><span data-stu-id="6f8d8-138">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="6f8d8-139">Преобразования баз данных</span><span class="sxs-lookup"><span data-stu-id="6f8d8-139">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




