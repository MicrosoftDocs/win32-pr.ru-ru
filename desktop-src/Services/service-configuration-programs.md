---
description: Программисты и системные администраторы используют программы настройки служб для изменения или запроса базы данных установленных служб.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Программы настройки служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad7ef3efffb185b2d29c6eab496bf76d12343a0e16f845702e910695220b048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967708"
---
# <a name="service-configuration-programs"></a>Программы настройки служб

Программисты и системные администраторы используют программы настройки служб для изменения или запроса базы данных установленных служб. Доступ к базе данных также можно получить с помощью функций реестра. Однако следует использовать только функции конфигурации SCM, которые гарантируют правильную установку и настройку службы.

Функции конфигурации SCM должны быть либо обработчиком объекта SCManager, либо маркером для объекта службы. Для получения этих дескрипторов программа настройки службы должна:

1.  Используйте функцию [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) для получения маркера базы данных SCM на указанном компьютере.
2.  Используйте функцию [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) или [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для получения маркера объекта службы.

Дополнительные сведения см. в следующих разделах:

-   [Установка, удаление и перечисление служб](service-installation-removal-and-enumeration.md)
-   [Конфигурация службы.](service-configuration.md)
-   [Настройка службы с помощью SC](configuring-a-service-using-sc.md)

 

 



