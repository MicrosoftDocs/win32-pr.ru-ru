---
description: Запускается программа управления службами, которая управляет службами.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Программы управления службами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897150"
---
# <a name="service-control-programs"></a>Программы управления службами

Запускается программа управления службами, которая управляет службами. Он выполняет следующие действия:

-   Запускает службу или драйвер, если тип запуска — \_ Запуск по запросу службы \_ .
-   Отправляет управляющие запросы в работающую службу.
-   Запрашивает текущее состояние выполняющейся службы.

Для этих действий требуется открытый обработчик для объекта службы. Для получения этого маркера программа управления службой должна:

1.  Используйте функцию [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) для получения маркера базы данных SCM на указанном компьютере.
2.  Используйте функцию [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) или [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для получения маркера объекта службы.

Дополнительные сведения см. в следующих разделах:

-   [Запуск службы](service-startup.md)
-   [Запросы управления службами](service-control-requests.md)
-   [Управление службой с помощью SC](controlling-a-service-using-sc.md)

 

 



