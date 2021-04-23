---
description: В таблице CheckBox перечислены значения флажков.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Таблица флажков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662905"
---
# <a name="checkbox-table"></a><span data-ttu-id="23bdb-103">Таблица флажков</span><span class="sxs-lookup"><span data-stu-id="23bdb-103">CheckBox Table</span></span>

<span data-ttu-id="23bdb-104">В таблице CheckBox перечислены значения флажков.</span><span class="sxs-lookup"><span data-stu-id="23bdb-104">The CheckBox table lists the values for the check boxes.</span></span>

<span data-ttu-id="23bdb-105">Таблица CheckBox содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="23bdb-105">The CheckBox table has the following columns.</span></span>



| <span data-ttu-id="23bdb-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="23bdb-106">Column</span></span>   | <span data-ttu-id="23bdb-107">Type</span><span class="sxs-lookup"><span data-stu-id="23bdb-107">Type</span></span>                         | <span data-ttu-id="23bdb-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="23bdb-108">Key</span></span> | <span data-ttu-id="23bdb-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="23bdb-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="23bdb-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="23bdb-110">Property</span></span> | [<span data-ttu-id="23bdb-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="23bdb-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="23bdb-112">Да</span><span class="sxs-lookup"><span data-stu-id="23bdb-112">Y</span></span>   | <span data-ttu-id="23bdb-113">Нет</span><span class="sxs-lookup"><span data-stu-id="23bdb-113">N</span></span>        |
| <span data-ttu-id="23bdb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="23bdb-114">Value</span></span>    | [<span data-ttu-id="23bdb-115">Формате</span><span class="sxs-lookup"><span data-stu-id="23bdb-115">Formatted</span></span>](formatted.md)   | <span data-ttu-id="23bdb-116">Нет</span><span class="sxs-lookup"><span data-stu-id="23bdb-116">N</span></span>   | <span data-ttu-id="23bdb-117">Да</span><span class="sxs-lookup"><span data-stu-id="23bdb-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="23bdb-118">Столбцы</span><span class="sxs-lookup"><span data-stu-id="23bdb-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="23bdb-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Свойства</span><span class="sxs-lookup"><span data-stu-id="23bdb-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="23bdb-120">Именованное свойство, которое должно быть привязано к этому элементу.</span><span class="sxs-lookup"><span data-stu-id="23bdb-120">A named property to be tied to this item.</span></span>

</dd> <dt>

<span data-ttu-id="23bdb-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="23bdb-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="23bdb-122">Строка значения, связанная с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="23bdb-122">The value string associated with this item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23bdb-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23bdb-123">Remarks</span></span>

<span data-ttu-id="23bdb-124">Если установлен флажок, то соответствующее свойство устанавливается в указанное значение.</span><span class="sxs-lookup"><span data-stu-id="23bdb-124">If the check box is selected, then the corresponding property is set to the specified value.</span></span> <span data-ttu-id="23bdb-125">Если значение не указано или таблица не существует, свойство устанавливается в исходное значение, если установлен флажок.</span><span class="sxs-lookup"><span data-stu-id="23bdb-125">If there is no value specified or this table does not exist, then the property is set to its original value when the check box is selected.</span></span> <span data-ttu-id="23bdb-126">Если исходное значение равно null, свойство имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="23bdb-126">If the original value is null, the property is set to "1".</span></span>

<span data-ttu-id="23bdb-127">Содержимое столбца значений форматируется функцией [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) при создании элемента управления.</span><span class="sxs-lookup"><span data-stu-id="23bdb-127">The contents of the Value column are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created.</span></span> <span data-ttu-id="23bdb-128">Поэтому он может содержать любое выражение, которое может интерпретировать функция **мсиформатрекорд** .</span><span class="sxs-lookup"><span data-stu-id="23bdb-128">Therefore, it can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="23bdb-129">Столбец значение форматируется только при создании элемента управления и не обновляется, если свойство, вовлеченное в выражение, изменяется в течение жизненного цикла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="23bdb-129">The Value column is formatted only when the control is created, and it is not updated if a property involved in an expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="23bdb-130">Проверка</span><span class="sxs-lookup"><span data-stu-id="23bdb-130">Validation</span></span>

<dl>

[<span data-ttu-id="23bdb-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="23bdb-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="23bdb-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="23bdb-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="23bdb-133">ICE46</span><span class="sxs-lookup"><span data-stu-id="23bdb-133">ICE46</span></span>](ice46.md)  
</dl>

 

 



