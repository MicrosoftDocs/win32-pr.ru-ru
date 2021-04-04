---
description: Таблица Ресервекост — это необязательная таблица, позволяющая автору резервировать объем дискового пространства в любом каталоге, который зависит от состояния установки компонента.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: Таблица Ресервекост
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998742"
---
# <a name="reservecost-table"></a><span data-ttu-id="98912-103">Таблица Ресервекост</span><span class="sxs-lookup"><span data-stu-id="98912-103">ReserveCost Table</span></span>

<span data-ttu-id="98912-104">Таблица Ресервекост — это необязательная таблица, позволяющая автору резервировать объем дискового пространства в любом каталоге, который зависит от состояния установки компонента.</span><span class="sxs-lookup"><span data-stu-id="98912-104">The ReserveCost table is an optional table that allows the author to reserve an amount of disk space in any directory that depends on the installation state of a component.</span></span>

<span data-ttu-id="98912-105">Таблица Ресервекост содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="98912-105">The ReserveCost table has the following columns.</span></span>



| <span data-ttu-id="98912-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="98912-106">Column</span></span>        | <span data-ttu-id="98912-107">Type</span><span class="sxs-lookup"><span data-stu-id="98912-107">Type</span></span>                               | <span data-ttu-id="98912-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="98912-108">Key</span></span> | <span data-ttu-id="98912-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="98912-109">Nullable</span></span> |
|---------------|------------------------------------|-----|----------|
| <span data-ttu-id="98912-110">ресервекэй</span><span class="sxs-lookup"><span data-stu-id="98912-110">ReserveKey</span></span>    | [<span data-ttu-id="98912-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="98912-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="98912-112">Да</span><span class="sxs-lookup"><span data-stu-id="98912-112">Y</span></span>   | <span data-ttu-id="98912-113">Нет</span><span class="sxs-lookup"><span data-stu-id="98912-113">N</span></span>        |
| <span data-ttu-id="98912-114">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="98912-114">Component\_</span></span>   | [<span data-ttu-id="98912-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="98912-115">Identifier</span></span>](identifier.md)       | <span data-ttu-id="98912-116">Нет</span><span class="sxs-lookup"><span data-stu-id="98912-116">N</span></span>   | <span data-ttu-id="98912-117">Нет</span><span class="sxs-lookup"><span data-stu-id="98912-117">N</span></span>        |
| <span data-ttu-id="98912-118">ресервефолдер</span><span class="sxs-lookup"><span data-stu-id="98912-118">ReserveFolder</span></span> | [<span data-ttu-id="98912-119">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="98912-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="98912-120">Нет</span><span class="sxs-lookup"><span data-stu-id="98912-120">N</span></span>   | <span data-ttu-id="98912-121">Да</span><span class="sxs-lookup"><span data-stu-id="98912-121">Y</span></span>        |
| <span data-ttu-id="98912-122">ресервелокал</span><span class="sxs-lookup"><span data-stu-id="98912-122">ReserveLocal</span></span>  | [<span data-ttu-id="98912-123">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="98912-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="98912-124">Нет</span><span class="sxs-lookup"><span data-stu-id="98912-124">N</span></span>   | <span data-ttu-id="98912-125">Нет</span><span class="sxs-lookup"><span data-stu-id="98912-125">N</span></span>        |
| <span data-ttu-id="98912-126">ресервесаурце</span><span class="sxs-lookup"><span data-stu-id="98912-126">ReserveSource</span></span> | [<span data-ttu-id="98912-127">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="98912-127">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="98912-128">Нет</span><span class="sxs-lookup"><span data-stu-id="98912-128">N</span></span>   | <span data-ttu-id="98912-129">Нет</span><span class="sxs-lookup"><span data-stu-id="98912-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="98912-130">Столбцы</span><span class="sxs-lookup"><span data-stu-id="98912-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="98912-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ресервекэй</span><span class="sxs-lookup"><span data-stu-id="98912-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span></span>
</dt> <dd>

<span data-ttu-id="98912-132">Первичный ключ, однозначно определяющий запись таблицы Ресервекост.</span><span class="sxs-lookup"><span data-stu-id="98912-132">Primary key that uniquely identifies a ReserveCost table entry.</span></span>

</dd> <dt>

<span data-ttu-id="98912-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="98912-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="98912-134">Внешний ключ к столбцу одной из таблиц [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="98912-134">External key to column one of the [Component](component-table.md) table.</span></span> <span data-ttu-id="98912-135">Резервирует заданный объем пространства, если компонент должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="98912-135">Reserves a specified amount of space if this component is to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="98912-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ресервефолдер</span><span class="sxs-lookup"><span data-stu-id="98912-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span></span>
</dt> <dd>

<span data-ttu-id="98912-137">Этот столбец содержит имя свойства, которое является полным путем к целевому каталогу.</span><span class="sxs-lookup"><span data-stu-id="98912-137">This column contains the name of a property that is the full path to the destination directory.</span></span> <span data-ttu-id="98912-138">Это имя свойства обычно является именем каталога в таблице [Directory](directory-table.md) или именем набора свойств, полученного с помощью действия [аппсеарч](appsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="98912-138">This property name is typically the name of a directory in the [Directory](directory-table.md) table or the name of a property set obtained using the [Appsearch](appsearch-action.md) action.</span></span> <span data-ttu-id="98912-139">Это увеличивает объем дискового пространства, указанный в Ресервелокал или Ресервесаурце, на стоимость тома устройства, содержащего каталог.</span><span class="sxs-lookup"><span data-stu-id="98912-139">This adds the amount of disk space specified in ReserveLocal or ReserveSource to the volume cost of the device containing the directory.</span></span>

</dd> <dt>

<span data-ttu-id="98912-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ресервелокал</span><span class="sxs-lookup"><span data-stu-id="98912-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span></span>
</dt> <dd>

<span data-ttu-id="98912-141">Количество байтов дискового пространства, резервируемое при установке связанного компонента для локального запуска.</span><span class="sxs-lookup"><span data-stu-id="98912-141">The number of bytes of disk space to reserve if the linked component is installed to run locally.</span></span>

</dd> <dt>

<span data-ttu-id="98912-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ресервесаурце</span><span class="sxs-lookup"><span data-stu-id="98912-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span></span>
</dt> <dd>

<span data-ttu-id="98912-143">Число байтов дискового пространства, резервируемое при установке связанного компонента для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="98912-143">The number of bytes of disk space to reserve if the linked component is installed to run from source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98912-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98912-144">Remarks</span></span>

<span data-ttu-id="98912-145">Резервирование затрат таким образом может быть полезно для авторов, желающих убедиться, что после завершения установки будет доступен минимальный объем дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="98912-145">Reserving cost in this way could be useful for authors who want to ensure that a minimum amount of disk space will be available after the installation is completed.</span></span> <span data-ttu-id="98912-146">Например, это место на диске может быть зарезервировано для документов пользователя или файлов приложения (например, файлов индекса), созданных только после запуска приложения после установки.</span><span class="sxs-lookup"><span data-stu-id="98912-146">For example, this disk space might be reserved for user documents or for application files (such as index files) that are created only after the application is started following installation.</span></span>

<span data-ttu-id="98912-147">С помощью таблицы Ресервекост можно включить настраиваемые действия, чтобы указать приблизительную стоимость для файлов, записей реестра или других элементов, которые может устанавливать пользовательское действие.</span><span class="sxs-lookup"><span data-stu-id="98912-147">You can use the ReserveCost table to enable custom actions to specify an approximate cost for any files, registry entries, or other items that the custom action might install.</span></span> <span data-ttu-id="98912-148">Пользовательские действия, добавляющие записи в таблицу Ресервекост, должны быть упорядочены между действиями [костинитиализе](costinitialize-action.md) и [филекост](filecost-action.md) .</span><span class="sxs-lookup"><span data-stu-id="98912-148">Custom actions that add entries to the ReserveCost table should be sequenced between the [CostInitialize](costinitialize-action.md) and [FileCost](filecost-action.md) actions.</span></span> <span data-ttu-id="98912-149">Это необходимо для того, чтобы действие Филекост правильно инициализировать стоимость всех компонентов, затронутых записями в таблице Ресервекост.</span><span class="sxs-lookup"><span data-stu-id="98912-149">This is necessary for the FileCost action to correctly initialize the costing of all components affected by entries in the ReserveCost table.</span></span>

## <a name="validation"></a><span data-ttu-id="98912-150">Проверка</span><span class="sxs-lookup"><span data-stu-id="98912-150">Validation</span></span>

<dl>

[<span data-ttu-id="98912-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="98912-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="98912-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="98912-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="98912-153">ICE32</span><span class="sxs-lookup"><span data-stu-id="98912-153">ICE32</span></span>](ice32.md)  
</dl>

 

 



