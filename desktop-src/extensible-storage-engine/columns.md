---
description: 'Дополнительные сведения: столбцы'
title: Столбцы
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 86f7d2bbb3925434ddbfff52e987b6e408af9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155054"
---
# <a name="columns"></a><span data-ttu-id="4f803-103">Столбцы</span><span class="sxs-lookup"><span data-stu-id="4f803-103">Columns</span></span>


<span data-ttu-id="4f803-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4f803-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="columns"></a><span data-ttu-id="4f803-105">Столбцы</span><span class="sxs-lookup"><span data-stu-id="4f803-105">Columns</span></span>

<span data-ttu-id="4f803-106">Таблицу можно создать либо с начальным набором столбцов, вызвав [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md) , либо без начального набора столбцов путем вызова [жеткреатетабле](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="4f803-106">A table can be created either with an initial set of columns by calling [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or without an initial set of columns by calling [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="4f803-107">Таблицы в подсистеме ESE могут содержать до 127 столбцов фиксированной длины, 128 столбцов переменной длины и 64 993 столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="4f803-107">Tables in ESE can contain up to 127 fixed-length columns, 128 variable-length columns, and 64,993 tagged columns.</span></span> <span data-ttu-id="4f803-108">Столбцы идентифицируются по имени и ИДЕНТИФИКАТОРу и могут динамически добавляться в таблицу с помощью [жетаддколумн](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="4f803-108">Columns are identified by their name and ID and can be dynamically added to the table with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="4f803-109">Столбцы создаются с определенным типом данных и необязательным набором атрибутов, например, имеет ли столбец фиксированную длину или может принимать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4f803-109">Columns are created with a specific data type and an optional set of attributes, such as whether the column is fixed-length or whether it can be NULL or not.</span></span>

<span data-ttu-id="4f803-110">Тип столбца определяет данные, которые могут храниться в столбце, и многие свойства столбца, включая его порядок для индексирования.</span><span class="sxs-lookup"><span data-stu-id="4f803-110">The type of a column determines the data that may be stored in the column and many of the properties of the column, including its order for indexing.</span></span> <span data-ttu-id="4f803-111">ESE поддерживает широкий спектр типов столбцов, от 1 до 2 ГБ (2146483647 символов ASCII или 1073741823 символов Юникода).</span><span class="sxs-lookup"><span data-stu-id="4f803-111">ESE supports a wide range of column types, ranging in size from 1 bit to 2 GB (2146483647 ASCII characters or 1073741823 Unicode characters).</span></span> <span data-ttu-id="4f803-112">Полный список типов данных столбцов, поддерживаемых ESE, см. в [JET_COLTYP](./jet-coltyp.md) разделе.</span><span class="sxs-lookup"><span data-stu-id="4f803-112">For a complete list of the column data types supported by ESE, see the [JET_COLTYP](./jet-coltyp.md) topic.</span></span> <span data-ttu-id="4f803-113">В следующих разделах обсуждаются некоторые типы столбцов, поддерживаемые ESE:</span><span class="sxs-lookup"><span data-stu-id="4f803-113">The topics below discuss a few of the columns types supported by ESE:</span></span>

  - [<span data-ttu-id="4f803-114">Столбцы с тегами, фиксированными и переменными</span><span class="sxs-lookup"><span data-stu-id="4f803-114">Tagged, Fixed and Variable Columns</span></span>](./tagged-fixed-and-variable-columns.md)

  - [<span data-ttu-id="4f803-115">Версия, автоматический инкремент и столбцы с подстолбцами</span><span class="sxs-lookup"><span data-stu-id="4f803-115">Version, Auto-Increment and Escrow Columns</span></span>](./version-auto-increment-and-escrow-columns.md)

  - [<span data-ttu-id="4f803-116">Столбцы с длинными значениями</span><span class="sxs-lookup"><span data-stu-id="4f803-116">Long Value Columns</span></span>](./long-value-columns.md)

  - [<span data-ttu-id="4f803-117">Разреженные столбцы с несколькими значениями</span><span class="sxs-lookup"><span data-stu-id="4f803-117">Multi-Valued Sparse Columns</span></span>](./multi-valued-sparse-columns.md)

  - [<span data-ttu-id="4f803-118">Определяемые пользователем столбцы</span><span class="sxs-lookup"><span data-stu-id="4f803-118">User Defined Columns</span></span>](./user-defined-columns.md)

  - [<span data-ttu-id="4f803-119">Использование столбцов в таблице</span><span class="sxs-lookup"><span data-stu-id="4f803-119">Using Columns in a Table</span></span>](./using-columns-in-a-table.md)
