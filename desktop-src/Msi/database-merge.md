---
description: Метод Merge объекта Database выполняет слияние эталонной базы данных с базовой базой данных.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database. Merge, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652045"
---
# <a name="databasemerge-method"></a><span data-ttu-id="ff4f9-103">Database. Merge, метод</span><span class="sxs-lookup"><span data-stu-id="ff4f9-103">Database.Merge method</span></span>

<span data-ttu-id="ff4f9-104">Метод **Merge** объекта [**Database**](database-object.md) выполняет слияние эталонной базы данных с базовой базой данных.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-104">The **Merge** method of the [**Database**](database-object.md) object merges the reference database with the base database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff4f9-105">Syntax</span></span>


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a><span data-ttu-id="ff4f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff4f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff4f9-107">*reference*</span><span class="sxs-lookup"><span data-stu-id="ff4f9-107">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="ff4f9-108">Требуемый объект [**базы данных**](database-object.md) для слияния с базой данных.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-108">The required [**Database**](database-object.md) object to be merged into the database.</span></span>

</dd> <dt>

<span data-ttu-id="ff4f9-109">*еррортабле*</span><span class="sxs-lookup"><span data-stu-id="ff4f9-109">*errorTable*</span></span> 
</dt> <dd>

<span data-ttu-id="ff4f9-110">Необязательное имя таблицы, содержащей имена таблиц, содержащих конфликты слияния, число конфликтующих строк в таблице, а также ссылку на таблицу с конфликтом слияния.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-110">An optional name of a table to contain the names of the tables containing merge conflicts, the number of conflicting rows within the table, and a reference to the table with the merge conflict.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff4f9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff4f9-111">Return value</span></span>

<span data-ttu-id="ff4f9-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff4f9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff4f9-113">Remarks</span></span>

<span data-ttu-id="ff4f9-114">Функцию [**мсидатабасемерже**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) и метод **Merge** объекта [**Database**](database-object.md) нельзя использовать для слияния модулей, входящих в пакет установки.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-114">The [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function and the **Merge** method of the [**Database**](database-object.md) object cannot be used to merge a module included within an installation package.</span></span> <span data-ttu-id="ff4f9-115">Их не следует использовать для слияния [модулей слияния](merge-modules.md) в пакет установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-115">They should not be used to merge [Merge Modules](merge-modules.md) into a Windows Installer package.</span></span> <span data-ttu-id="ff4f9-116">Чтобы включить модуль слияния в пакет установки, авторы пакетов установки должны следовать рекомендациям, описанным в разделе [применение модулей слияния](applying-merge-modules.md) .</span><span class="sxs-lookup"><span data-stu-id="ff4f9-116">To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in the [Applying Merge Modules](applying-merge-modules.md) topic.</span></span>

<span data-ttu-id="ff4f9-117">Метод **Merge** не копирует встроенные CAB- [файлы](cabinet-files.md) или [встроенные преобразования](embedded-transforms.md) из эталонной базы данных в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-117">The **Merge** method does not copy over embedded [cabinet files](cabinet-files.md) or [embedded transforms](embedded-transforms.md) from the reference database into the target database.</span></span> <span data-ttu-id="ff4f9-118">Внедренные потоки данных, перечисленные в таблице [двоичной таблицы](binary-table.md) или [значка](icon-table.md) , копируются из эталонной базы данных в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-118">Embedded data streams that are listed in the [Binary Table](binary-table.md) or [Icon Table](icon-table.md) are copied from the reference database to the target database.</span></span> <span data-ttu-id="ff4f9-119">Хранилища, внедренные в эталонную базу данных, не копируются в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-119">Storages embedded in the reference database are not copied to the target database.</span></span>

<span data-ttu-id="ff4f9-120">Если таблица не указана, общее сообщение об ошибке содержит количество таблиц, содержащих конфликты слияния.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-120">If no table is provided, the general error message provides the number of tables containing merge conflicts.</span></span> <span data-ttu-id="ff4f9-121">Любая таблица может быть передана, но все остальные столбцы должны допускать значение null, так как операция обновления [таблицы ошибок](error-table.md) завершается ошибкой, если столбец не допускает значения NULL.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-121">Any table can be passed in, but all other columns must be nullable because the operation to update the [Error Table](error-table.md) fails if a column is not nullable.</span></span> <span data-ttu-id="ff4f9-122">Вновь созданную таблицу можно также передать, так как метод **Merge** автоматически создает используемые столбцы при обнаружении конфликтов слияния.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-122">A newly created table can be passed in as well because the **Merge** method automatically creates the columns it uses if merge conflicts are found.</span></span> <span data-ttu-id="ff4f9-123">Для представления конфликтов слияния используются два столбца.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-123">Two columns are used to present merge conflicts.</span></span> <span data-ttu-id="ff4f9-124">Первый столбец — это имя таблицы и первичный ключевой столбец.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-124">The first column is the table name and the primary key column.</span></span> <span data-ttu-id="ff4f9-125">Второй столбец — это число строк в этой таблице, которые содержат ошибки слияния.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-125">The second column is the number of rows of that table that have merge failures.</span></span>

<span data-ttu-id="ff4f9-126">Если таблицы с одинаковыми именами в обеих базах данных не совпадают в количестве первичных ключей, типах столбцов, количестве столбцов или именах столбцов, метод **Merge** завершается ошибкой и отправляет сообщение об ошибке, сообщающее, что произошло.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-126">If tables of the same name in both databases do not match in the number of primary keys, the column types, the number of columns, or the column names, the **Merge** method fails and posts an error message stating what occurred.</span></span>

<span data-ttu-id="ff4f9-127">Чтобы Таблица ошибок оставалась неизменной, обработчик ошибок должен зафиксировать базу данных, к которой принадлежит таблица ошибок.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-127">For the Error table to remain, the error handler must commit the database to which the Error table belongs.</span></span> <span data-ttu-id="ff4f9-128">Однако эту фиксацию следует выполнять после использования третьего столбца для получения ссылок на таблицы, в которых возникли конфликты слияния.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-128">However, this commit should be done after using the third column to obtain the references to those tables where merge conflicts occurred.</span></span>

<span data-ttu-id="ff4f9-129">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="ff4f9-129">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff4f9-130">Требования</span><span class="sxs-lookup"><span data-stu-id="ff4f9-130">Requirements</span></span>



| <span data-ttu-id="ff4f9-131">Требование</span><span class="sxs-lookup"><span data-stu-id="ff4f9-131">Requirement</span></span> | <span data-ttu-id="ff4f9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ff4f9-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff4f9-133">Версия</span><span class="sxs-lookup"><span data-stu-id="ff4f9-133">Version</span></span><br/> | <span data-ttu-id="ff4f9-134">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ff4f9-135">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ff4f9-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ff4f9-136">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff4f9-136">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ff4f9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ff4f9-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="ff4f9-138"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff4f9-138"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ff4f9-139">IID</span><span class="sxs-lookup"><span data-stu-id="ff4f9-139">IID</span></span><br/>     | <span data-ttu-id="ff4f9-140">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ff4f9-140">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




