---
description: Метод Апплитрансформ объекта Database применяет преобразование к этой базе данных.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Database. Апплитрансформ, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669124"
---
# <a name="databaseapplytransform-method"></a><span data-ttu-id="327de-103">Database. Апплитрансформ, метод</span><span class="sxs-lookup"><span data-stu-id="327de-103">Database.ApplyTransform method</span></span>

<span data-ttu-id="327de-104">Метод **апплитрансформ** объекта [**Database**](database-object.md) применяет преобразование к этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="327de-104">The **ApplyTransform** method of the [**Database**](database-object.md) object applies the transform to this database.</span></span>

## <a name="syntax"></a><span data-ttu-id="327de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="327de-105">Syntax</span></span>


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a><span data-ttu-id="327de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="327de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="327de-107">*storage*</span><span class="sxs-lookup"><span data-stu-id="327de-107">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="327de-108">Путь к примененному файлу преобразования.</span><span class="sxs-lookup"><span data-stu-id="327de-108">Path to the transform file being applied.</span></span> <span data-ttu-id="327de-109">Этот параметр обязателен.</span><span class="sxs-lookup"><span data-stu-id="327de-109">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="327de-110">*ерроркондитионс*</span><span class="sxs-lookup"><span data-stu-id="327de-110">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="327de-111">Указывает условия ошибки, которые следует подавлять.</span><span class="sxs-lookup"><span data-stu-id="327de-111">Specifies the error conditions that are to be suppressed.</span></span> <span data-ttu-id="327de-112">Укажите как сочетание следующих целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="327de-112">Specify as a combination of the following integer values.</span></span>



| <span data-ttu-id="327de-113">Условие ошибки</span><span class="sxs-lookup"><span data-stu-id="327de-113">Error condition</span></span>                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="327de-114">Значение</span><span class="sxs-lookup"><span data-stu-id="327de-114">Meaning</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="327de-115"><dt>**мситрансформеррораддексистингров**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="327de-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span></span> </dl>                                 | <span data-ttu-id="327de-116">Добавляет уже существующую строку.</span><span class="sxs-lookup"><span data-stu-id="327de-116">Adds a row that already exists.</span></span><br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="327de-117"><dt>**мситрансформеррорделетенонексистингров**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="327de-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="327de-118">Удаляет несуществующую строку.</span><span class="sxs-lookup"><span data-stu-id="327de-118">Deletes a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="327de-119"><dt>**мситрансформеррораддексистингтабле**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="327de-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span></span> </dl>                         | <span data-ttu-id="327de-120">Добавляет уже существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="327de-120">Adds a table that already exists.</span></span><br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="327de-121"><dt>**мситрансформеррорделетенонексистингтабле**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="327de-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="327de-122">Удаляет несуществующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="327de-122">Deletes a table that does not exist.</span></span><br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="327de-123"><dt>**мситрансформеррорупдатенонексистингров**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="327de-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span></span> </dl>         | <span data-ttu-id="327de-124">Обновляет несуществующую строку.</span><span class="sxs-lookup"><span data-stu-id="327de-124">Updates a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="327de-125"><dt>**мситрансформеррорчанжекодепаже**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="327de-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span></span> </dl>                                 | <span data-ttu-id="327de-126">Кодовые страницы преобразований и баз данных не совпадают, и ни одна из них не имеет нейтральной кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="327de-126">Transform and database code pages do not match and neither has a neutral code page.</span></span><br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <span data-ttu-id="327de-127"><dt>**мситрансформеррорвиевтрансформ**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="327de-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span></span> </dl>                                     | <span data-ttu-id="327de-128">Создает временную [ \_ таблицу данных reformview](-transformview-table.md).</span><span class="sxs-lookup"><span data-stu-id="327de-128">Creates the temporary [\_TransformView table](-transformview-table.md).</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="327de-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="327de-129">Return value</span></span>

<span data-ttu-id="327de-130">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="327de-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="327de-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="327de-131">Remarks</span></span>

<span data-ttu-id="327de-132">Метод **апплитрансформ** задерживает Преобразование таблиц до последнего возможного момента.</span><span class="sxs-lookup"><span data-stu-id="327de-132">The **ApplyTransform** method delays transforming tables until the last possible moment.</span></span> <span data-ttu-id="327de-133">Шаги, выполняемые в **апплитрансформ** , позволяют немедленно преобразовать каталоги таблиц и столбцов для базы данных.</span><span class="sxs-lookup"><span data-stu-id="327de-133">The steps taken in **ApplyTransform** are to immediately transform the table and column catalogs for the database.</span></span> <span data-ttu-id="327de-134">Каталоги таблиц и столбцов обновляются в соответствии с добавлением или удалением таблицы и добавлением столбца (удаление столбцов запрещено).</span><span class="sxs-lookup"><span data-stu-id="327de-134">The table and column catalogs are updated according to which table is added or deleted and which column is added (no deletion of columns is allowed).</span></span> <span data-ttu-id="327de-135">Если таблица в данный момент загружена в память и ее необходимо преобразовать, она преобразуется.</span><span class="sxs-lookup"><span data-stu-id="327de-135">If a table is currently loaded in memory and needs to be transformed, it is transformed.</span></span> <span data-ttu-id="327de-136">В противном случае для состояния таблицы задается значение, для которого требуется преобразование, чтобы при загрузке таблицы или при фиксации базы данных было применено преобразование.</span><span class="sxs-lookup"><span data-stu-id="327de-136">Otherwise, the table state is set to that requiring a transform so that when the table is loaded, or when the database is committed, the transform is applied.</span></span> <span data-ttu-id="327de-137">Преобразование в этом экземпляре означает, что фактические (строки) данные таблицы добавляются, удаляются или обновляются.</span><span class="sxs-lookup"><span data-stu-id="327de-137">Transform in this instance means that the actual (row) data of the table is added, deleted, or updated.</span></span>

<span data-ttu-id="327de-138">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="327de-138">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="327de-139">Требования</span><span class="sxs-lookup"><span data-stu-id="327de-139">Requirements</span></span>



| <span data-ttu-id="327de-140">Требование</span><span class="sxs-lookup"><span data-stu-id="327de-140">Requirement</span></span> | <span data-ttu-id="327de-141">Значение</span><span class="sxs-lookup"><span data-stu-id="327de-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="327de-142">Версия</span><span class="sxs-lookup"><span data-stu-id="327de-142">Version</span></span><br/> | <span data-ttu-id="327de-143">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="327de-143">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="327de-144">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="327de-144">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="327de-145">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="327de-145">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="327de-146">DLL</span><span class="sxs-lookup"><span data-stu-id="327de-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="327de-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="327de-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="327de-148">IID</span><span class="sxs-lookup"><span data-stu-id="327de-148">IID</span></span><br/>     | <span data-ttu-id="327de-149">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="327de-149">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="327de-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="327de-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327de-151">**База данных**</span><span class="sxs-lookup"><span data-stu-id="327de-151">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="327de-152">Преобразования баз данных</span><span class="sxs-lookup"><span data-stu-id="327de-152">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




