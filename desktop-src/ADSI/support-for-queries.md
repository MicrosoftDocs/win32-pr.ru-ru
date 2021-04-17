---
title: Поддержка запросов
description: Реализуя интерфейс IDirectorySearch, поставщики ADSI получают доступ к подмножеству OLE DB функций только для чтения.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Поддержка запросов ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1304dcabd9c008b0f645982e695554225f59bac9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654099"
---
# <a name="support-for-queries"></a>Поддержка запросов

Реализуя интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , поставщики ADSI получают доступ к подмножеству OLE DB функций только для чтения.

Реализация ADSI методов [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) использует интерфейсы OLE DB, описанные в ADSI версии 1,0, включая следующий список COM-объектов.

-   Объект источника данных (Служба каталогов), поддерживающий **IDBInitialize**, **метода IDBCreateSession**, **интерфейс IDBProperties** и **IPersist**.
-   Объект Дбсессионс, поддерживающий **IOpenRowSet**, **исессионпропертиес** и **икреатекомманд**.
-   Объект Command, поддерживающий **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** и **Интерфейс IConvertType**.
-   Объект набора строк, поддерживающий **IAccessor**, **IColumnsInfo**, **Интерфейс IConvertType**, **IRowset** и **ировсетинфо**.

Дополнительные сведения о OLE DB см. в разделе Справочник программиста по OLE DB в пакете SDK для платформы.

 

 




