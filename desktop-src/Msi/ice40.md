---
description: ICE40 выполняет различные проверки.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156718"
---
# <a name="ice40"></a><span data-ttu-id="ca4f5-103">ICE40</span><span class="sxs-lookup"><span data-stu-id="ca4f5-103">ICE40</span></span>

<span data-ttu-id="ca4f5-104">ICE40 выполняет различные проверки.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-104">ICE40 does miscellaneous validation.</span></span>

## <a name="result"></a><span data-ttu-id="ca4f5-105">Результат</span><span class="sxs-lookup"><span data-stu-id="ca4f5-105">Result</span></span>

<span data-ttu-id="ca4f5-106">ICE40 отправляет предупреждения по следующим адресам:</span><span class="sxs-lookup"><span data-stu-id="ca4f5-106">ICE40 posts warnings on the following:</span></span>

-   <span data-ttu-id="ca4f5-107">Свойство [**REINSTALLMODE**](reinstallmode.md) было переопределено.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-107">The [**REINSTALLMODE**](reinstallmode.md) property has been overridden.</span></span>
-   <span data-ttu-id="ca4f5-108">[Таблица ремовеинифиле](removeinifile-table.md) содержит запись тега DELETE без значения.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-108">The [RemoveIniFile table](removeinifile-table.md) has a Delete Tag entry with no value.</span></span>
-   <span data-ttu-id="ca4f5-109">В MSI-файле отсутствует [Таблица ошибок](error-table.md) , а свойство " [**Сводка по количеству страниц**](page-count-summary.md) " меньше или равно 100.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-109">The .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <span data-ttu-id="ca4f5-110">Это предупреждение КОМПИЛЯТОРА устарело, так как установщик Windows не требует, чтобы пакет имел таблицу ошибок.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-110">This ICE warning is obsolete because Windows Installer does not require the package to have an Error table.</span></span> <span data-ttu-id="ca4f5-111">Сообщения об ошибках можно получить с помощью Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-111">Error messages can be retrieved using Msimsg.dll.</span></span>

## <a name="example"></a><span data-ttu-id="ca4f5-112">Пример</span><span class="sxs-lookup"><span data-stu-id="ca4f5-112">Example</span></span>

[<span data-ttu-id="ca4f5-113">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="ca4f5-113">Property Table</span></span>](property-table.md)



| <span data-ttu-id="ca4f5-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="ca4f5-114">Property</span></span>                               | <span data-ttu-id="ca4f5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ca4f5-115">Value</span></span> |
|----------------------------------------|-------|
| [<span data-ttu-id="ca4f5-116">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="ca4f5-116">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="ca4f5-117">Объект</span><span class="sxs-lookup"><span data-stu-id="ca4f5-117">A</span></span>     |



 

[<span data-ttu-id="ca4f5-118">Таблица Ремовеинифиле</span><span class="sxs-lookup"><span data-stu-id="ca4f5-118">RemoveIniFile Table</span></span>](removeinifile-table.md)



| <span data-ttu-id="ca4f5-119">ремовеинифиле</span><span class="sxs-lookup"><span data-stu-id="ca4f5-119">RemoveIniFile</span></span>                          | <span data-ttu-id="ca4f5-120">Действие</span><span class="sxs-lookup"><span data-stu-id="ca4f5-120">Action</span></span> | <span data-ttu-id="ca4f5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ca4f5-121">Value</span></span> |
|----------------------------------------|--------|-------|
| [<span data-ttu-id="ca4f5-122">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="ca4f5-122">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="ca4f5-123">4</span><span class="sxs-lookup"><span data-stu-id="ca4f5-123">4</span></span>      |       |



 

## <a name="results"></a><span data-ttu-id="ca4f5-124">Результаты</span><span class="sxs-lookup"><span data-stu-id="ca4f5-124">Results</span></span>

<span data-ttu-id="ca4f5-125">ICE40 сообщит о следующих ошибках.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-125">ICE40 would report the following errors.</span></span>



| <span data-ttu-id="ca4f5-126">ICE40, ошибка</span><span class="sxs-lookup"><span data-stu-id="ca4f5-126">ICE40 error</span></span>                                                                                           | <span data-ttu-id="ca4f5-127">Описание</span><span class="sxs-lookup"><span data-stu-id="ca4f5-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4f5-128">[**REINSTALLMODE**](reinstallmode.md) определяется в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-128">[**REINSTALLMODE**](reinstallmode.md) is defined in the Property table.</span></span> <span data-ttu-id="ca4f5-129">Это может вызвать проблемы.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-129">This may cause difficulties.</span></span> | <span data-ttu-id="ca4f5-130">Определение свойства [**REINSTALLMODE**](reinstallmode.md) в MSI File может привести к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-130">Defining the [**REINSTALLMODE**](reinstallmode.md) property in .msi file can lead to unexpected behavior.</span></span> <span data-ttu-id="ca4f5-131">Чтобы устранить эту ошибку, не определяйте это свойство.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-131">To fix this error, do not define this property.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ca4f5-132">Запись Ремовеинифиле Remove1 должна иметь значение, так как действие "удалить тег" (4).</span><span class="sxs-lookup"><span data-stu-id="ca4f5-132">RemoveIniFile entry Remove1 must have a value, because the Action is "Delete Tag" (4).</span></span>                | <span data-ttu-id="ca4f5-133">В столбце Ремовеинифиле [таблицы ремовеинифиле](removeinifile-table.md) имеется действие Удалить тег, не указывая тег для удаления в столбце значение.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-133">There is a Delete Tag action in the in the RemoveIniFile column of the [RemoveIniFile table](removeinifile-table.md) without specifying a tag to delete in the Value column.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ca4f5-134">Отсутствует таблица ошибок.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-134">Error Table is missing.</span></span> <span data-ttu-id="ca4f5-135">Будут созданы только числовые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-135">Only numerical error messages will be generated.</span></span>                              | <span data-ttu-id="ca4f5-136">Это предупреждение КОМПИЛЯТОРА устарело, так как установщик Windows не требует, чтобы пакет имел [таблицу ошибок](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="ca4f5-136">This ICE warning is obsolete because Windows Installer does not require the package to have an [Error table](error-table.md).</span></span> <span data-ttu-id="ca4f5-137">Сообщения об ошибках можно получить с помощью Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-137">Error messages can be retrieved using Msimsg.dll.</span></span><br/> <span data-ttu-id="ca4f5-138">Это предупреждение означает, что в MSI-файле отсутствует [Таблица ошибок](error-table.md) , а свойство " [**Сводка по количеству страниц**](page-count-summary.md) " меньше или равно 100.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-138">This warning means that the .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <br/> <span data-ttu-id="ca4f5-139">Чтобы устранить эту ошибку, используйте текущую версию установщик Windows или добавьте таблицу ошибок в пакет установки и создайте шаблоны форматирования в столбце сообщение для сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="ca4f5-139">To fix this error, use a current version of the Windows Installer, or add an Error table to the installation package and author formatting templates in the Message column for error messages.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ca4f5-140">См. также</span><span class="sxs-lookup"><span data-stu-id="ca4f5-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca4f5-141">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="ca4f5-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




