---
description: Метод Креатетрансформсуммаринфо объекта Database создает и заполняет поток сводных данных существующего файла преобразования. Этот метод заполняет свойства базовыми и ссылочными ProductCode и ProductVersion.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Database. Креатетрансформсуммаринфо, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665427"
---
# <a name="databasecreatetransformsummaryinfo-method"></a><span data-ttu-id="a77e4-104">Database. Креатетрансформсуммаринфо, метод</span><span class="sxs-lookup"><span data-stu-id="a77e4-104">Database.CreateTransformSummaryInfo method</span></span>

<span data-ttu-id="a77e4-105">Метод **креатетрансформсуммаринфо** объекта [**Database**](database-object.md) создает и заполняет поток сводных данных существующего файла преобразования.</span><span class="sxs-lookup"><span data-stu-id="a77e4-105">The **CreateTransformSummaryInfo** method of the [**Database**](database-object.md) object creates and populates the summary information stream of an existing transform file.</span></span> <span data-ttu-id="a77e4-106">Этот метод заполняет свойства базовыми и ссылочными [**ProductCode**](productcode.md) и [**ProductVersion**](productversion.md).</span><span class="sxs-lookup"><span data-stu-id="a77e4-106">This method fills in the properties with the base and reference [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a77e4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a77e4-107">Syntax</span></span>


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a><span data-ttu-id="a77e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a77e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a77e4-109">*reference*</span><span class="sxs-lookup"><span data-stu-id="a77e4-109">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="a77e4-110">Требуемая база данных, не включающая изменения.</span><span class="sxs-lookup"><span data-stu-id="a77e4-110">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="a77e4-111">*storage*</span><span class="sxs-lookup"><span data-stu-id="a77e4-111">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="a77e4-112">Имя созданного файла преобразования.</span><span class="sxs-lookup"><span data-stu-id="a77e4-112">The name of the generated transform file.</span></span> <span data-ttu-id="a77e4-113">Это необязательно.</span><span class="sxs-lookup"><span data-stu-id="a77e4-113">This is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a77e4-114">*ерроркондитионс*</span><span class="sxs-lookup"><span data-stu-id="a77e4-114">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="a77e4-115">Обязательные условия ошибки, которые следует подавлять при применении преобразования.</span><span class="sxs-lookup"><span data-stu-id="a77e4-115">Required error conditions that should be suppressed when the transform is applied.</span></span> <span data-ttu-id="a77e4-116">Объедините одно или несколько следующих значений условий ошибки.</span><span class="sxs-lookup"><span data-stu-id="a77e4-116">Combine one or more of the following error condition values.</span></span>



| <span data-ttu-id="a77e4-117">Имя условия ошибки</span><span class="sxs-lookup"><span data-stu-id="a77e4-117">Error condition name</span></span>                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="a77e4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a77e4-118">Meaning</span></span>                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <span data-ttu-id="a77e4-119"><dt>**мситрансформеррорноне**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span></span> </dl>                                                                         | <span data-ttu-id="a77e4-120">Ни одно из следующих условий не задано.</span><span class="sxs-lookup"><span data-stu-id="a77e4-120">None of the following conditions.</span></span><br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="a77e4-121"><dt>**мситрансформеррораддексистингров**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span></span> </dl>                                 | <span data-ttu-id="a77e4-122">Добавляет уже существующую строку.</span><span class="sxs-lookup"><span data-stu-id="a77e4-122">Adds a row that already exists.</span></span><br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="a77e4-123"><dt>**мситрансформеррорделетенонексистингров**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="a77e4-124">Удаляет несуществующую строку.</span><span class="sxs-lookup"><span data-stu-id="a77e4-124">Deletes a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="a77e4-125"><dt>**мситрансформеррораддексистингтабле**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="a77e4-126">Добавляет уже существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="a77e4-126">Adds a table that already exists.</span></span><br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="a77e4-127"><dt>**мситрансформеррорделетенонексистингтабле**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="a77e4-128">Удаляет несуществующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="a77e4-128">Deletes a table that does not exist.</span></span><br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="a77e4-129"><dt>**мситрансформеррорупдатенонексистингров**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span></span> </dl>        | <span data-ttu-id="a77e4-130">Обновляет несуществующую строку.</span><span class="sxs-lookup"><span data-stu-id="a77e4-130">Updates a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="a77e4-131"><dt>**мситрансформеррорчанжекодепаже**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span></span> </dl>                                | <span data-ttu-id="a77e4-132">Кодовые страницы преобразований и баз данных не совпадают, и ни одна кодовая страница не является нейтральной.</span><span class="sxs-lookup"><span data-stu-id="a77e4-132">Transform and database code pages do not match and neither code page is neutral.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a77e4-133">*validation*</span><span class="sxs-lookup"><span data-stu-id="a77e4-133">*validation*</span></span> 
</dt> <dd>

<span data-ttu-id="a77e4-134">Требуется при применении преобразования к базе данных. показывает, какие свойства должны быть проверены, чтобы убедиться, что это преобразование может быть применено к базе данных.</span><span class="sxs-lookup"><span data-stu-id="a77e4-134">Required when the transform is applied to a database; shows which properties should be validated to verify that this transform can be applied to the database.</span></span> <span data-ttu-id="a77e4-135">Все свойства содержатся в [наборе свойств потока сводных данных](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="a77e4-135">The properties are all contained in the [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="a77e4-136">Объедините одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a77e4-136">Combine one or more of the following values.</span></span>



| <span data-ttu-id="a77e4-137">Флаг проверки</span><span class="sxs-lookup"><span data-stu-id="a77e4-137">Validation flag</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="a77e4-138">Значение</span><span class="sxs-lookup"><span data-stu-id="a77e4-138">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <span data-ttu-id="a77e4-139"><dt>**мситрансформвалидатионноне**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="a77e4-140">Проверка не выполнена.</span><span class="sxs-lookup"><span data-stu-id="a77e4-140">No validation done.</span></span><br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <span data-ttu-id="a77e4-141"><dt>**мситрансформвалидатионлангуаже**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="a77e4-142">Язык по умолчанию должен соответствовать базовой базе данных.</span><span class="sxs-lookup"><span data-stu-id="a77e4-142">Default language must match base database.</span></span><br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <span data-ttu-id="a77e4-143"><dt>**мситрансформвалидатионпродукт**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="a77e4-144">Продукт должен соответствовать базовой базе данных.</span><span class="sxs-lookup"><span data-stu-id="a77e4-144">Product must match base database.</span></span><br/>          |



 

<span data-ttu-id="a77e4-145">Чтобы проверить версию продукта, сначала выберите один или несколько из этих трех флагов, чтобы указать, какая часть версии должна быть проверена.</span><span class="sxs-lookup"><span data-stu-id="a77e4-145">To validate product version, first choose one or more of these three flags to indicate how much of the version is to be verified.</span></span>



| <span data-ttu-id="a77e4-146">Флаг проверки</span><span class="sxs-lookup"><span data-stu-id="a77e4-146">Validation flag</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="a77e4-147">Значение</span><span class="sxs-lookup"><span data-stu-id="a77e4-147">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <span data-ttu-id="a77e4-148"><dt>**мситрансформвалидатионмажорвер**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span></span> </dl>      | <span data-ttu-id="a77e4-149">Проверяет только основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="a77e4-149">Checks major version only.</span></span><br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <span data-ttu-id="a77e4-150"><dt>**мситрансформвалидатионминорвер**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span></span> </dl>     | <span data-ttu-id="a77e4-151">Проверяет только основной и дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="a77e4-151">Checks major and minor version only.</span></span><br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <span data-ttu-id="a77e4-152"><dt>**мситрансформвалидатионупдатевер**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span></span> </dl> | <span data-ttu-id="a77e4-153">Проверяет основные, дополнительные и обновленные версии.</span><span class="sxs-lookup"><span data-stu-id="a77e4-153">Checks major, minor, and update versions.</span></span><br/> |



 

<span data-ttu-id="a77e4-154">Затем выберите один из следующих элементов, чтобы указать требуемую связь между версией продукта базы данных, к которой применяется преобразование, и базой данных в базовой базе.</span><span class="sxs-lookup"><span data-stu-id="a77e4-154">Then choose one of the following to indicate the required relationship between the product version of the database the transform is being applied to and that of the base database.</span></span>



| <span data-ttu-id="a77e4-155">Флаг проверки</span><span class="sxs-lookup"><span data-stu-id="a77e4-155">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="a77e4-156">Значение</span><span class="sxs-lookup"><span data-stu-id="a77e4-156">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <span data-ttu-id="a77e4-157"><dt>**мситрансформвалидатионлесс**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span></span> </dl>                                          | <span data-ttu-id="a77e4-158">Примененная версия < базовая версия</span><span class="sxs-lookup"><span data-stu-id="a77e4-158">Applied version < base version</span></span><br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <span data-ttu-id="a77e4-159"><dt>**мситрансформвалидатионлессорекуал**</dt> <dt>128</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span></span> </dl>             | <span data-ttu-id="a77e4-160">Примененная версия <= базовая версия</span><span class="sxs-lookup"><span data-stu-id="a77e4-160">Applied version <= base version</span></span><br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <span data-ttu-id="a77e4-161"><dt>**мситрансформвалидатионекуал**</dt> <dt>256</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span></span> </dl>                                     | <span data-ttu-id="a77e4-162">Примененная версия = базовая версия</span><span class="sxs-lookup"><span data-stu-id="a77e4-162">Applied version = base version</span></span><br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <span data-ttu-id="a77e4-163"><dt>**мситрансформвалидатионгреатерорекуал**</dt> <dt>512</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span></span> </dl> | <span data-ttu-id="a77e4-164">Примененная версия >= базовая версия</span><span class="sxs-lookup"><span data-stu-id="a77e4-164">Applied version >= base version</span></span><br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <span data-ttu-id="a77e4-165"><dt>**мситрансформвалидатионгреатер**</dt> <dt>1024</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span></span> </dl>                            | <span data-ttu-id="a77e4-166">Примененная версия > базовая версия</span><span class="sxs-lookup"><span data-stu-id="a77e4-166">Applied version > base version</span></span><br/>  |



 

<span data-ttu-id="a77e4-167">Чтобы убедиться, что преобразование применяется к пакету с соответствующим параметром [**UpgradeCode**](upgradecode.md), установите следующий флаг.</span><span class="sxs-lookup"><span data-stu-id="a77e4-167">To validate that the transform is being applied to a package having the appropriate [**UpgradeCode**](upgradecode.md), set the following flag.</span></span>



| <span data-ttu-id="a77e4-168">Флаг проверки</span><span class="sxs-lookup"><span data-stu-id="a77e4-168">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="a77e4-169">Значение</span><span class="sxs-lookup"><span data-stu-id="a77e4-169">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <span data-ttu-id="a77e4-170"><dt>**мситрансформвалидатионупградекоде**</dt> <dt>2048</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span></span> </dl> | <span data-ttu-id="a77e4-171">Проверяет, что преобразование является соответствующим параметром [**UpgradeCode**](upgradecode.md).</span><span class="sxs-lookup"><span data-stu-id="a77e4-171">Validates that the transform is the appropriate [**UpgradeCode**](upgradecode.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a77e4-172">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a77e4-172">Return value</span></span>

<span data-ttu-id="a77e4-173">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a77e4-173">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a77e4-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a77e4-174">Remarks</span></span>

<span data-ttu-id="a77e4-175">Чтобы создать информационный поток сводки для преобразования, свойства [**ProductCode**](productcode.md) и [**ProductVersion**](productversion.md) должны быть определены в таблицах [свойств](property-table.md) базовых и эталонных баз данных.</span><span class="sxs-lookup"><span data-stu-id="a77e4-175">To create a summary information stream for a transform, the [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md) properties must be defined in the [Property](property-table.md) tables of both the base and reference databases.</span></span> <span data-ttu-id="a77e4-176">Если используется Мситрансформвалидатионупградекоде, свойство [**UpgradeCode**](upgradecode.md) должно быть определено в обеих базах данных.</span><span class="sxs-lookup"><span data-stu-id="a77e4-176">If msiTransformValidationUpgradeCode is used, the [**UpgradeCode**](upgradecode.md) property must be defined in both databases.</span></span>

## <a name="requirements"></a><span data-ttu-id="a77e4-177">Требования</span><span class="sxs-lookup"><span data-stu-id="a77e4-177">Requirements</span></span>



| <span data-ttu-id="a77e4-178">Требование</span><span class="sxs-lookup"><span data-stu-id="a77e4-178">Requirement</span></span> | <span data-ttu-id="a77e4-179">Значение</span><span class="sxs-lookup"><span data-stu-id="a77e4-179">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a77e4-180">Версия</span><span class="sxs-lookup"><span data-stu-id="a77e4-180">Version</span></span><br/> | <span data-ttu-id="a77e4-181">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a77e4-181">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a77e4-182">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a77e4-182">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a77e4-183">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="a77e4-183">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a77e4-184">DLL</span><span class="sxs-lookup"><span data-stu-id="a77e4-184">DLL</span></span><br/>     | <dl> <span data-ttu-id="a77e4-185"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a77e4-185"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a77e4-186">IID</span><span class="sxs-lookup"><span data-stu-id="a77e4-186">IID</span></span><br/>     | <span data-ttu-id="a77e4-187">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a77e4-187">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="a77e4-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a77e4-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a77e4-189">Преобразования баз данных</span><span class="sxs-lookup"><span data-stu-id="a77e4-189">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




