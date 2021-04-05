---
description: HKLM \\ программное обеспечение \\ \\ клиента Microsoft MSSQLSERVER \\ .
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: SsASnoversion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072421"
---
# <a name="connectto"></a>SsASnoversion

**HKLM \\ программное обеспечение \\ \\ клиента Microsoft MSSQLSERVER \\**

## <a name="description"></a>Описание

В подразделе **ssASnoversion** хранятся сведения о соединении для клиентов под управлением Windows, подключающихся к экземплярам компонента ядра СУБД Microsoft SQL Server. Записи реестра в этом подразделе имеют тип данных REG \_ SZ, а их значения указывают Net-Library, используемые для подключения к экземпляру, а также любые параметры, относящиеся к сети.

Сведения о подключении, хранящиеся в этом подразделе, считываются поставщиком OLE DB для SQL Server, драйвером SQL Server ODBC или библиотекой динамической компоновки SQL Server DB-Library (DLL).

## <a name="change-method"></a>Изменение метода

Не следует изменять записи в этом подразделе с помощью редактора реестра. Чтобы настроить имя сервера и сведения о соединении, используйте служебную программу клиента SQL Server Network. Дополнительные сведения см. в справке программы SQL Server Client Network.

## <a name="notes"></a>Примечания

-   Подключ **ssASnoversion** используется поставщиком OLE DB для SQL Server, драйвером SQL Server ODBC и SQL Server DB-Library DLL. Записи в этом подразделе указывают, какие Net-Library вызывают эти компоненты API доступа к данным.
-   Net-Libraries являются компонентами SQL Server, которые защищают компоненты API доступа к данным из подробных сведений об использовании различных методов межпроцессного взаимодействия (IPC) для взаимодействия с экземпляром ядра СУБД SQL Server.
-   Неправильное обновление подраздела **ssASnoversion** может препятствовать успешному подключению приложений к экземпляру компонента ядра СУБД SQL Server.

 

 



