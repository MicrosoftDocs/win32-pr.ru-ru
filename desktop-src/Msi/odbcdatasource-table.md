---
description: В таблице Одбкдатасаурце перечислены источники данных, принадлежащие установке.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Таблица Одбкдатасаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673368"
---
# <a name="odbcdatasource-table"></a><span data-ttu-id="77660-103">Таблица Одбкдатасаурце</span><span class="sxs-lookup"><span data-stu-id="77660-103">ODBCDataSource Table</span></span>

<span data-ttu-id="77660-104">В таблице Одбкдатасаурце перечислены источники данных, принадлежащие установке.</span><span class="sxs-lookup"><span data-stu-id="77660-104">The ODBCDataSource table lists the data sources belonging to the installation.</span></span>

<span data-ttu-id="77660-105">Таблица Одбкдатасаурце содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="77660-105">The ODBCDataSource table has the following columns.</span></span>



| <span data-ttu-id="77660-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="77660-106">Column</span></span>            | <span data-ttu-id="77660-107">Type</span><span class="sxs-lookup"><span data-stu-id="77660-107">Type</span></span>                         | <span data-ttu-id="77660-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="77660-108">Key</span></span> | <span data-ttu-id="77660-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="77660-109">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="77660-110">DataSource</span><span class="sxs-lookup"><span data-stu-id="77660-110">DataSource</span></span>        | [<span data-ttu-id="77660-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="77660-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="77660-112">Да</span><span class="sxs-lookup"><span data-stu-id="77660-112">Y</span></span>   | <span data-ttu-id="77660-113">Нет</span><span class="sxs-lookup"><span data-stu-id="77660-113">N</span></span>        |
| <span data-ttu-id="77660-114">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="77660-114">Component\_</span></span>       | [<span data-ttu-id="77660-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="77660-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="77660-116">Нет</span><span class="sxs-lookup"><span data-stu-id="77660-116">N</span></span>   | <span data-ttu-id="77660-117">Нет</span><span class="sxs-lookup"><span data-stu-id="77660-117">N</span></span>        |
| <span data-ttu-id="77660-118">Описание</span><span class="sxs-lookup"><span data-stu-id="77660-118">Description</span></span>       | [<span data-ttu-id="77660-119">Text</span><span class="sxs-lookup"><span data-stu-id="77660-119">Text</span></span>](text.md)             | <span data-ttu-id="77660-120">Нет</span><span class="sxs-lookup"><span data-stu-id="77660-120">N</span></span>   | <span data-ttu-id="77660-121">Нет</span><span class="sxs-lookup"><span data-stu-id="77660-121">N</span></span>        |
| <span data-ttu-id="77660-122">дривердескриптион</span><span class="sxs-lookup"><span data-stu-id="77660-122">DriverDescription</span></span> | [<span data-ttu-id="77660-123">Text</span><span class="sxs-lookup"><span data-stu-id="77660-123">Text</span></span>](text.md)             | <span data-ttu-id="77660-124">Нет</span><span class="sxs-lookup"><span data-stu-id="77660-124">N</span></span>   | <span data-ttu-id="77660-125">Нет</span><span class="sxs-lookup"><span data-stu-id="77660-125">N</span></span>        |
| <span data-ttu-id="77660-126">Регистрация</span><span class="sxs-lookup"><span data-stu-id="77660-126">Registration</span></span>      | [<span data-ttu-id="77660-127">Integer</span><span class="sxs-lookup"><span data-stu-id="77660-127">Integer</span></span>](integer.md)       | <span data-ttu-id="77660-128">Нет</span><span class="sxs-lookup"><span data-stu-id="77660-128">N</span></span>   | <span data-ttu-id="77660-129">Нет</span><span class="sxs-lookup"><span data-stu-id="77660-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="77660-130">Столбцы</span><span class="sxs-lookup"><span data-stu-id="77660-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="77660-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span><span class="sxs-lookup"><span data-stu-id="77660-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span></span>
</dt> <dd>

<span data-ttu-id="77660-132">Имя внутреннего маркера для источника данных.</span><span class="sxs-lookup"><span data-stu-id="77660-132">Internal token name for data source.</span></span> <span data-ttu-id="77660-133">Первичный ключ для таблицы.</span><span class="sxs-lookup"><span data-stu-id="77660-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="77660-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="77660-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="77660-135">Внешний ключ в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="77660-135">External key into the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="77660-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="77660-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="77660-137">Описание, зарегистрированное для этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="77660-137">The description registered for this data source.</span></span> <span data-ttu-id="77660-138">Это значение не может быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="77660-138">This value cannot be localized.</span></span> <span data-ttu-id="77660-139">Описания источников данных ODBC не могут превышать \_ максимальную \_ длину имени DSN SQL \_ .</span><span class="sxs-lookup"><span data-stu-id="77660-139">ODBC data source descriptions cannot exceed SQL\_MAX\_DSN\_LENGTH.</span></span>

</dd> <dt>

<span data-ttu-id="77660-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>дривердескриптион</span><span class="sxs-lookup"><span data-stu-id="77660-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span></span>
</dt> <dd>

<span data-ttu-id="77660-141">Связанный драйвер, который может быть предварительно создан.</span><span class="sxs-lookup"><span data-stu-id="77660-141">Associated driver which may be pre-existing.</span></span> <span data-ttu-id="77660-142">Это значение не может быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="77660-142">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="77660-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="77660-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registration</span></span>
</dt> <dd>

<span data-ttu-id="77660-144">В этом поле указывается тип регистрации для источника данных.</span><span class="sxs-lookup"><span data-stu-id="77660-144">This field specifies the type of registration for the data source.</span></span>



| <span data-ttu-id="77660-145">Константа</span><span class="sxs-lookup"><span data-stu-id="77660-145">Constant</span></span>                                      | <span data-ttu-id="77660-146">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="77660-146">Hexadecimal</span></span> | <span data-ttu-id="77660-147">Decimal</span><span class="sxs-lookup"><span data-stu-id="77660-147">Decimal</span></span> | <span data-ttu-id="77660-148">Описание</span><span class="sxs-lookup"><span data-stu-id="77660-148">Description</span></span>                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| <span data-ttu-id="77660-149">**мсидбодбкдатасаурцерегистратионпермачине**</span><span class="sxs-lookup"><span data-stu-id="77660-149">**msidbODBCDataSourceRegistrationPerMachine**</span></span> | <span data-ttu-id="77660-150">0x000</span><span class="sxs-lookup"><span data-stu-id="77660-150">0x000</span></span>       | <span data-ttu-id="77660-151">0</span><span class="sxs-lookup"><span data-stu-id="77660-151">0</span></span>       | <span data-ttu-id="77660-152">Источник данных регистрируется на компьютере.</span><span class="sxs-lookup"><span data-stu-id="77660-152">Data source is registered per machine.</span></span> |
| <span data-ttu-id="77660-153">**мсидбодбкдатасаурцерегистратионперусер**</span><span class="sxs-lookup"><span data-stu-id="77660-153">**msidbODBCDataSourceRegistrationPerUser**</span></span>    | <span data-ttu-id="77660-154">0x001</span><span class="sxs-lookup"><span data-stu-id="77660-154">0x001</span></span>       | <span data-ttu-id="77660-155">1</span><span class="sxs-lookup"><span data-stu-id="77660-155">1</span></span>       | <span data-ttu-id="77660-156">Источник данных регистрируется для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="77660-156">Data source is registered per user.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77660-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77660-157">Remarks</span></span>

<span data-ttu-id="77660-158">Действия [инсталлодбк](installodbc-action.md) и [ремовеодбк](removeodbc-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="77660-158">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="77660-159">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="77660-159">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="77660-160">Проверка</span><span class="sxs-lookup"><span data-stu-id="77660-160">Validation</span></span>

<dl>

[<span data-ttu-id="77660-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="77660-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="77660-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="77660-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="77660-163">ICE32</span><span class="sxs-lookup"><span data-stu-id="77660-163">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="77660-164">ICE45</span><span class="sxs-lookup"><span data-stu-id="77660-164">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="77660-165">ICE98</span><span class="sxs-lookup"><span data-stu-id="77660-165">ICE98</span></span>](ice98.md)  
</dl>

 

 



