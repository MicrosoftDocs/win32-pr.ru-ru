---
description: API однорангового распространения определяет следующие типы данных.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Типы данных API однорангового распространения
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663318"
---
# <a name="peer-distribution-api-data-types"></a>Типы данных API однорангового распространения

API однорангового распространения определяет следующие типы данных.


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| Тип данных                                                                                                                     | Описание                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_маркер экземпляра для класса, \_**          | Маркер, связанный с экземпляром распространения однорангового узла. Этот обработчик создается [**пирдистстартуп**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)и используется в большинстве операций распространения одноранговых узлов.<br/>                                          |
| <span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_маркер содержимого для объекта, \_**             | Маркер, связанный с содержимым. Этот обработчик создается [**пирдистклиентопенконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) , и на него указывают ссылки при открытии, закрытии, добавлении или публикации содержимого.<br/>                     |
| <span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_Handle контентинфо \_** | Маркер, связанный со сведениями о содержимом. Этот обработчик создается [**пирдистсерверопенконтентинформатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)и используется при извлечении сведений о кодированном содержимом.<br/> |
| <span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_Handle Stream \_**                | Маркер, связанный с потоком данных. Этот маркер создается [**пирдистсерверпублишстреам**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) , и на него указывают ссылки при публикации, закрытии или добавлении в потоковый контент.<br/>        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 7 Профессиональная\]<br/>                               |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>В видеом для. h</dt> </dl> |



 

 




