---
description: Служба однорангового распространения (Майкрософт) поддерживает следующие структуры.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Структуры API однорангового распространения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663315"
---
# <a name="peer-distribution-api-structures"></a>Структуры API однорангового распространения

Служба однорангового распространения (Майкрософт) поддерживает следующие структуры.



| Структура                                                              | Описание                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ основные \_ сведения о клиенте WebClient**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | Указывает, существует ли несколько клиентов, одновременно загружая одно и то же содержимое.                                                                                                                                                                                             |
| [**\_тег содержимого для объекта, \_**](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | Содержит тег, предоставляемый клиентом, который является входным значением для [**пирдистклиентопенконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent). Тег связан с сегментом содержимого и используется в API-интерфейсах управления содержимым, например [**пирдистклиентфлушконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent). |
| [**\_Параметры публикации в \_ свойствах,**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | Содержит параметры публикации, включая сведения о версии API и возможные флаги параметров.                                                                                                                                                                                           |
| [**\_Параметры получения ОДНОранговых узлов \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | Содержит версию сведений о содержимом для извлечения.                                                                                                                                                                                                                                 |
| [**\_сведения о состоянии сведений о том, \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | Содержит сведения о текущем состоянии и возможностях службы BranchCache на локальном компьютере.                                                                                                                                                                         |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по API однорангового распространения](peer-distribution-api-reference.md)
</dt> </dl>

 

 



