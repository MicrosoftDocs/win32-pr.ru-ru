---
title: Обработка результирующего набора
description: Результирующий набор возвращается в виде последовательности строк.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339228"
---
# <a name="processing-a-result-set"></a><span data-ttu-id="d0e8b-103">Обработка результирующего набора</span><span class="sxs-lookup"><span data-stu-id="d0e8b-103">Processing a Result Set</span></span>

<span data-ttu-id="d0e8b-104">Результирующий набор возвращается в виде последовательности строк.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-104">A result set is returned as a series of rows.</span></span> <span data-ttu-id="d0e8b-105">Каждая строка может не содержать заданный атрибут.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-105">Each row may or may not contain a given attribute.</span></span> <span data-ttu-id="d0e8b-106">При использовании поставщика OLE DB результирующий набор будет похож на стандартный результирующий набор SQL.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-106">With the OLE DB provider, the result set appears similar to a normal SQL result set.</span></span> <span data-ttu-id="d0e8b-107">При использовании ADO для запроса объект [ADODB. Объект Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) используется для обхода результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-107">If you use ADO for the query, the [ADODB.Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) object is used for traversing the result set.</span></span> <span data-ttu-id="d0e8b-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (доступно только на языках, поддерживающих привязки vtable) содержит элементы для перемещения курсора строки и проверки значений свойств в заданной строке.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (available only from languages that support vtable bindings) contains members for moving the row cursor and checking property values in a given row.</span></span> <span data-ttu-id="d0e8b-109">Кроме того, можно использовать [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) для получения и задания свойств.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-109">Alternatively, you can use [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) to get and set properties.</span></span>

 

 