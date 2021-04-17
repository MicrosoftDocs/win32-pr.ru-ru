---
description: Приложения могут использовать PDH для извлечения счетчиков производительности из журналов SQL, а также извлекать форматированные или необработанные счетчики непосредственно из базы данных с помощью запросов SQL.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: Схема файла журнала SQL
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663148"
---
# <a name="sql-log-file-schema"></a>Схема файла журнала SQL

> [!IMPORTANT]
> Поддержка PDH для баз данных SQL ODBC может быть изменена или недоступна в будущем.

Приложения могут использовать интерфейсы API PDH для чтения и записи данных счетчиков производительности в совместимых базах данных SQL ODBC, а затем выполняют дальнейшую обработку с помощью запросов SQL. В этом разделе описывается схема SQL, используемая для хранения счетчиков производительности. Эти сведения можно использовать для создания пользовательских представлений и отчетов. Схема состоит из следующих трех таблиц:

- [**каунтердата**](counterdata.md)
- [**каунтердетаилс**](counterdetails.md)
- [**дисплайтоид**](displaytoid.md)

> [!NOTE]
> Поддержка PDH для баз данных SQL ODBC работает только с драйверами ODBC SQL, поддерживающими [расширения для операций с массовым копированием (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).
