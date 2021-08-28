---
title: TLS_HANDLE
description: Представляет маркер сервера лицензий удаленный рабочий стол.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04daf14429a5b400267e664a615739fd14e8306e987f50726cfdb341522870a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869454"
---
# <a name="tls_handle"></a>\_маркер TLS

Представляет маркер сервера лицензий удаленный рабочий стол. Этот маркер возвращается функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .

> [!Note]  
> Этот тип данных не имеет связанного файла заголовка. Чтобы использовать его, необходимо определить его самостоятельно, как показано в этом разделе.

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**тлсконнекттолссервер**](tlsconnecttolsserver.md)
</dt> <dt>

[**тлсдисконнектфромсервер**](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





