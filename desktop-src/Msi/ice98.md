---
description: ICE98 проверяет поле Description таблицы Одбкдатасаурце для источника данных ODBC. Она использует функцию Склвалиддсн, чтобы убедиться, что используются только допустимые символы, а описание не превышает максимально допустимой длины.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265047"
---
# <a name="ice98"></a><span data-ttu-id="7ad7a-104">ICE98</span><span class="sxs-lookup"><span data-stu-id="7ad7a-104">ICE98</span></span>

<span data-ttu-id="7ad7a-105">ICE98 проверяет поле Description [таблицы одбкдатасаурце](odbcdatasource-table.md) для источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="7ad7a-105">ICE98 verifies the description field of the [ODBCDataSource Table](odbcdatasource-table.md) for an ODBC data source.</span></span> <span data-ttu-id="7ad7a-106">Она использует функцию **склвалиддсн** , чтобы убедиться, что используются только допустимые символы, а описание не превышает максимально допустимой длины.</span><span class="sxs-lookup"><span data-stu-id="7ad7a-106">It uses the **SQLValidDSN** function to check that only valid characters are used, and that the description does not exceed the maximum allowed length.</span></span>

## <a name="result"></a><span data-ttu-id="7ad7a-107">Результат</span><span class="sxs-lookup"><span data-stu-id="7ad7a-107">Result</span></span>

<span data-ttu-id="7ad7a-108">ICE98 отправляет следующие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="7ad7a-108">ICE98 posts the following warnings.</span></span>



| <span data-ttu-id="7ad7a-109">Предупреждение ICE98</span><span class="sxs-lookup"><span data-stu-id="7ad7a-109">ICE98 warning</span></span>                    | <span data-ttu-id="7ad7a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7ad7a-110">Description</span></span>                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad7a-111">Недопустимое имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="7ad7a-111">The data source name is invalid.</span></span> | <span data-ttu-id="7ad7a-112">Значение в столбце Description [таблицы одбкдатасаурце](odbcdatasource-table.md) либо содержит недопустимые символы, либо имеет слишком большую длину, что означает, что он превышает \_ максимальную \_ длину DSN ( \_ 32) для SQL.</span><span class="sxs-lookup"><span data-stu-id="7ad7a-112">The value in the Description column of the [ODBCDataSource Table](odbcdatasource-table.md) either contains invalid characters or is too long, which means that it exceeds the SQL\_MAX\_DSN\_LENGTH of 32.</span></span> |



 

## <a name="example"></a><span data-ttu-id="7ad7a-113">Пример</span><span class="sxs-lookup"><span data-stu-id="7ad7a-113">Example</span></span>

<span data-ttu-id="7ad7a-114">ICE98 сообщает о следующих предупреждениях для примера:</span><span class="sxs-lookup"><span data-stu-id="7ad7a-114">ICE98 reports the following warnings for the example:</span></span>

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

<span data-ttu-id="7ad7a-115">[Таблица одбкдатасаурце](odbcdatasource-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="7ad7a-115">[ODBCDataSource Table](odbcdatasource-table.md) (partial)</span></span>



| <span data-ttu-id="7ad7a-116">DataSource</span><span class="sxs-lookup"><span data-stu-id="7ad7a-116">DataSource</span></span> | <span data-ttu-id="7ad7a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7ad7a-117">Description</span></span>                      |
|------------|----------------------------------|
| <span data-ttu-id="7ad7a-118">бадчар</span><span class="sxs-lookup"><span data-stu-id="7ad7a-118">BadChar</span></span>    | <span data-ttu-id="7ad7a-119">!</span><span class="sxs-lookup"><span data-stu-id="7ad7a-119">!</span></span>                                |
| <span data-ttu-id="7ad7a-120">тулонг</span><span class="sxs-lookup"><span data-stu-id="7ad7a-120">TooLong</span></span>    | <span data-ttu-id="7ad7a-121"><String of length > 32></span><span class="sxs-lookup"><span data-stu-id="7ad7a-121"><String of length > 32></span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7ad7a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7ad7a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ad7a-123">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="7ad7a-123">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="7ad7a-124">Таблица Одбкдатасаурце</span><span class="sxs-lookup"><span data-stu-id="7ad7a-124">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
</dt> </dl>

 

 



