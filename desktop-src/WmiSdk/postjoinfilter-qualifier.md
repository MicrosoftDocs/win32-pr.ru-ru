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
ms.openlocfilehash: be491c0bfefe77c2bf016789786212047d5ca8d00570c84057b8e8e346fb382e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317028"
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

 

