---
description: ICE45 проверяет, что столбцы битовых полей в базе данных не задают Зарезервированные биты равными 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264182"
---
# <a name="ice45"></a><span data-ttu-id="549e0-103">ICE45</span><span class="sxs-lookup"><span data-stu-id="549e0-103">ICE45</span></span>

<span data-ttu-id="549e0-104">ICE45 проверяет, что столбцы битовых полей в базе данных не задают Зарезервированные биты равными 1.</span><span class="sxs-lookup"><span data-stu-id="549e0-104">ICE45 validates that bit field columns in the database do not set any reserved bits to 1.</span></span>

<span data-ttu-id="549e0-105">Зарезервированные биты не предоставляют функциональных возможностей в текущих версиях установщика, но могут в будущих версиях.</span><span class="sxs-lookup"><span data-stu-id="549e0-105">Reserved bits provide no functionality in current versions of the installer, but might in future versions.</span></span> <span data-ttu-id="549e0-106">Для них необходимо задать значение 0, чтобы они были совместимы с будущими версиями установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="549e0-106">They should be set to 0 to be compatible with future versions of Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="549e0-107">Результат</span><span class="sxs-lookup"><span data-stu-id="549e0-107">Result</span></span>

<span data-ttu-id="549e0-108">ICE45 отправляет сообщение об ошибке, если любая из следующих таблиц содержит битовое поле, для которого зарезервированный бит имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="549e0-108">ICE45 posts an error message if any of the following tables contains a bit field with a reserved bit set to a value of 1.</span></span>

-   [<span data-ttu-id="549e0-109">Таблица Ббконтрол</span><span class="sxs-lookup"><span data-stu-id="549e0-109">BBControl table</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="549e0-110">Таблица диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="549e0-110">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="549e0-111">Таблица функций</span><span class="sxs-lookup"><span data-stu-id="549e0-111">Feature table</span></span>](feature-table.md)
-   [<span data-ttu-id="549e0-112">Таблица файлов</span><span class="sxs-lookup"><span data-stu-id="549e0-112">File table</span></span>](file-table.md)
-   [<span data-ttu-id="549e0-113">Таблица MoveFile</span><span class="sxs-lookup"><span data-stu-id="549e0-113">MoveFile table</span></span>](movefile-table.md)
-   [<span data-ttu-id="549e0-114">Таблица Модулеконфигуратион</span><span class="sxs-lookup"><span data-stu-id="549e0-114">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)
-   [<span data-ttu-id="549e0-115">Таблица Одбкдатасаурце</span><span class="sxs-lookup"><span data-stu-id="549e0-115">ODBCDataSource table</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="549e0-116">Таблица исправлений</span><span class="sxs-lookup"><span data-stu-id="549e0-116">Patch table</span></span>](patch-table.md)
-   [<span data-ttu-id="549e0-117">Таблица Ремовефиле</span><span class="sxs-lookup"><span data-stu-id="549e0-117">RemoveFile table</span></span>](removefile-table.md)
-   [<span data-ttu-id="549e0-118">Таблица ServiceControl</span><span class="sxs-lookup"><span data-stu-id="549e0-118">ServiceControl table</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="549e0-119">Таблица Сервицеинсталл</span><span class="sxs-lookup"><span data-stu-id="549e0-119">ServiceInstall table</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="549e0-120">Таблица система создала шрифт</span><span class="sxs-lookup"><span data-stu-id="549e0-120">TextStyle table</span></span>](textstyle-table.md)

<span data-ttu-id="549e0-121">ICE45 отправляет одно из двух предупреждений, если в [таблице элементов управления](control-table.md) содержится битовое поле с зарезервированным битом, равным значению 1.</span><span class="sxs-lookup"><span data-stu-id="549e0-121">ICE45 posts one of two warning messages if the [Control Table](control-table.md) contains a bit field with a reserved bit set to a value of 1.</span></span>

## <a name="example"></a><span data-ttu-id="549e0-122">Пример</span><span class="sxs-lookup"><span data-stu-id="549e0-122">Example</span></span>

<span data-ttu-id="549e0-123">ICE45 сообщает об ошибке в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="549e0-123">ICE45 reports the following error for the example shown.</span></span>

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

<span data-ttu-id="549e0-124">ICE45 сообщает следующее предупреждение для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="549e0-124">ICE45 reports the following warning for the example shown.</span></span>

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

<span data-ttu-id="549e0-125">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="549e0-125">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="549e0-126">Файл</span><span class="sxs-lookup"><span data-stu-id="549e0-126">File</span></span>  | <span data-ttu-id="549e0-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="549e0-127">Attributes</span></span> |
|-------|------------|
| <span data-ttu-id="549e0-128">Файл1</span><span class="sxs-lookup"><span data-stu-id="549e0-128">File1</span></span> | <span data-ttu-id="549e0-129">128</span><span class="sxs-lookup"><span data-stu-id="549e0-129">128</span></span>        |



 

<span data-ttu-id="549e0-130">[Таблица управления](control-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="549e0-130">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="549e0-131">Диалог</span><span class="sxs-lookup"><span data-stu-id="549e0-131">Dialog</span></span>  | <span data-ttu-id="549e0-132">Control</span><span class="sxs-lookup"><span data-stu-id="549e0-132">Control</span></span> | <span data-ttu-id="549e0-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="549e0-133">Attributes</span></span> |
|---------|---------|------------|
| <span data-ttu-id="549e0-134">Dialog1</span><span class="sxs-lookup"><span data-stu-id="549e0-134">Dialog1</span></span> | <span data-ttu-id="549e0-135">Edit1</span><span class="sxs-lookup"><span data-stu-id="549e0-135">Edit1</span></span>   | <span data-ttu-id="549e0-136">2097152</span><span class="sxs-lookup"><span data-stu-id="549e0-136">2097152</span></span>    |
| <span data-ttu-id="549e0-137">Dialog1</span><span class="sxs-lookup"><span data-stu-id="549e0-137">Dialog1</span></span> | <span data-ttu-id="549e0-138">Edit2</span><span class="sxs-lookup"><span data-stu-id="549e0-138">Edit2</span></span>   | <span data-ttu-id="549e0-139">1048576</span><span class="sxs-lookup"><span data-stu-id="549e0-139">1048576</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="549e0-140">См. также</span><span class="sxs-lookup"><span data-stu-id="549e0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="549e0-141">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="549e0-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



