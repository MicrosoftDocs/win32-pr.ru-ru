---
description: ICEM14 проверяет столбец значений таблицы Модулесубститутион.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155294"
---
# <a name="icem14"></a><span data-ttu-id="1a6ac-103">ICEM14</span><span class="sxs-lookup"><span data-stu-id="1a6ac-103">ICEM14</span></span>

<span data-ttu-id="1a6ac-104">ICEM14 проверяет столбец значений [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="1a6ac-104">ICEM14 validates the Value Column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="1a6ac-105">Результат</span><span class="sxs-lookup"><span data-stu-id="1a6ac-105">Result</span></span>

<span data-ttu-id="1a6ac-106">ICEM14 отправляет следующие ошибки.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-106">ICEM14 posts the following errors.</span></span>



| <span data-ttu-id="1a6ac-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="1a6ac-107">Error</span></span>                                                                                                                                                         | <span data-ttu-id="1a6ac-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1a6ac-108">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6ac-109">Строка замены в столбце Модулесубститутион. Value в строке \[ 1 \] . \[ 2 \] . \[ 3 \] не найден в таблице модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-109">The replacement string in ModuleSubstitution.Value column in row \[1\].\[2\].\[3\] is not found in ModuleConfiguration table.</span></span>                                 | <span data-ttu-id="1a6ac-110">\[1 \] . \[ 2 \] . \[ 3 \] ссылается на первичный ключ *Table. Row. Column* для строки в таблице модулесубститутион.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-110">\[1\].\[2\].\[3\] refers to a *table.row.column* primary key for a row in the ModuleSubstitution table.</span></span> <span data-ttu-id="1a6ac-111">Шаблон форматирования в поле значения этой строки не соответствует строке настраиваемых атрибутов в [таблице модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1a6ac-111">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                            |
| <span data-ttu-id="1a6ac-112">В таблице Модулесубститутион в строке \[ 1 \] . \[ 2 \] . \[ 3 \] . настраиваемый элемент указан в таблице "% s".</span><span class="sxs-lookup"><span data-stu-id="1a6ac-112">In ModuleSubstitution table in row \[1\].\[2\].\[3\], a configurable item is indicated in the table '%s'.</span></span> <span data-ttu-id="1a6ac-113">Таблица "% s" не должна содержать настраиваемые элементы.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-113">The table '%s' must not contain configurable items.</span></span> | <span data-ttu-id="1a6ac-114">Одна из следующих таблиц указана в столбце table таблицы Модулесубститутион: [модулесубститутион](modulesubstitution-table.md), [модулеконфигуратион](moduleconfiguration-table.md), [модуликсклусион](moduleexclusion-table.md)или [ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1a6ac-114">One of the following tables is listed in the Table column of the ModuleSubstitution table: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md), or [ModuleSignature](modulesignature-table.md).</span></span> <span data-ttu-id="1a6ac-115">Эти таблицы не могут содержать настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-115">These tables cannot contain configurable fields.</span></span> |
| <span data-ttu-id="1a6ac-116">В таблице Модулесубститутион в строке \[ 1 \] . \[ 2 \] . \[ 3 \] , указана пустая строка замены.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-116">In ModuleSubstitution table in row \[1\].\[2\].\[3\], an empty replacement string is specified.</span></span>                                                               | <span data-ttu-id="1a6ac-117">Шаблон форматирования в поле значения этой строки не соответствует строке настраиваемых атрибутов в [таблице модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1a6ac-117">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="1a6ac-118">ICEM14 отправляет следующее предупреждение.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-118">ICEM14 posts the following warning.</span></span>



| <span data-ttu-id="1a6ac-119">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="1a6ac-119">Warning</span></span>                                                                  | <span data-ttu-id="1a6ac-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1a6ac-120">Meaning</span></span>                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="1a6ac-121">Таблица Модулесубститутион существует, но отсутствует таблица Модулеконфигуратион</span><span class="sxs-lookup"><span data-stu-id="1a6ac-121">ModuleSubstitution table exists but ModuleConfiguration table is missing</span></span> | <span data-ttu-id="1a6ac-122">Таблица Модулеконфигуратион отсутствует.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-122">The ModuleConfiguration table is absent.</span></span> |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="1a6ac-123">Таблица, используемая во время выполнения</span><span class="sxs-lookup"><span data-stu-id="1a6ac-123">Table Used During Execution</span></span>

[<span data-ttu-id="1a6ac-124">Таблица Модулесубститутион</span><span class="sxs-lookup"><span data-stu-id="1a6ac-124">ModuleSubstitution table</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="1a6ac-125">Таблица Модулеконфигуратион</span><span class="sxs-lookup"><span data-stu-id="1a6ac-125">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)

## <a name="related-topics"></a><span data-ttu-id="1a6ac-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1a6ac-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a6ac-127">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="1a6ac-127">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



