---
description: Можно отфильтровать экземпляры класса представления соединений, назначив запрос WQL квалификатору Постжоинфилтер.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Квалификатор Постжоинфилтер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702659"
---
# <a name="postjoinfilter-qualifier"></a>Квалификатор Постжоинфилтер

Можно отфильтровать экземпляры класса представления соединений, назначив запрос WQL квалификатору **постжоинфилтер** . Значение WQL-запроса применяется к экземплярам класса представления JOIN. Этот квалификатор можно использовать, чтобы ограничить экземпляры класса представления теми, которые соответствуют определенным условиям. Следующий запрос WQL фильтрует экземпляры класса JOIN, вызываемые на основе экземпляров [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



Существует несколько ограничений на использование этого квалификатора.

-   **Постжоинфилтер** доступен только для классов представлений JOIN.
-   Имя класса и имена свойств, указанные в запросе, относятся к свойствам класса представления, а не к исходному классу.
-   Исключение свойств не разрешено; допускаются только `SELECT *` запросы типа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Квалификаторы, относящиеся к поставщику представления**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

