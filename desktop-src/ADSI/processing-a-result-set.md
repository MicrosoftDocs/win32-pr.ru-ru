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
# <a name="processing-a-result-set"></a>Обработка результирующего набора

Результирующий набор возвращается в виде последовательности строк. Каждая строка может не содержать заданный атрибут. При использовании поставщика OLE DB результирующий набор будет похож на стандартный результирующий набор SQL. При использовании ADO для запроса объект [ADODB. Объект Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) используется для обхода результирующего набора. [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (доступно только на языках, поддерживающих привязки vtable) содержит элементы для перемещения курсора строки и проверки значений свойств в заданной строке. Кроме того, можно использовать [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) для получения и задания свойств.

 

 