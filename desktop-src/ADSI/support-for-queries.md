---
title: Поддержка запросов
description: Реализуя интерфейс IDirectorySearch, поставщики ADSI получают доступ к подмножеству OLE DB функций только для чтения.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Поддержка запросов ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ad1892cf7c0e619ef55b9c3e5af6885d4cbdc7ac68fbcbd206524128b283d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023232"
---
# <a name="support-for-queries"></a>Поддержка запросов

Реализуя интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , поставщики ADSI получают доступ к подмножеству OLE DB функций только для чтения.

Реализация ADSI методов [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) использует интерфейсы OLE DB, описанные в ADSI версии 1,0, включая следующий список COM-объектов.

-   Объект источника данных (Служба каталогов), поддерживающий **IDBInitialize**, **метода IDBCreateSession**, **интерфейс IDBProperties** и **IPersist**.
-   Объект Дбсессионс, поддерживающий **IOpenRowSet**, **исессионпропертиес** и **икреатекомманд**.
-   Объект Command, поддерживающий **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** и **Интерфейс IConvertType**.
-   Объект набора строк, поддерживающий **IAccessor**, **IColumnsInfo**, **Интерфейс IConvertType**, **IRowset** и **ировсетинфо**.

Дополнительные сведения о OLE DB см. в разделе Справочник программиста по OLE DB в пакете SDK для платформы.

 

 




