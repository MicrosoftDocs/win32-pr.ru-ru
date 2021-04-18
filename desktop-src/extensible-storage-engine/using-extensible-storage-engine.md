---
description: 'Дополнительные сведения о: использование расширенного подсистемы хранилища'
title: Использование расширенного подсистемы хранилища
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 636c3fa96692b8c48f9a175b5fa7d34c53314e1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711578"
---
# <a name="using-extensible-storage-engine"></a>Использование расширенного подсистемы хранилища


_**Применимо к:** Windows | Windows Server_

## <a name="using-extensible-storage-engine"></a>Использование расширенного подсистемы хранилища

В этом разделе содержатся общие сведения об использовании следующих частей API ESE.

  - [Столбцы](./columns.md)

  - [Индексирование в таблице](./indexing-in-the-table.md)

  - [Создание баз данных](./creating-databases.md)

  - [Транзакции](./transactions.md)

  - [Ошибки ESE](./extensible-storage-engine-errors.md)

  - [Файлы ESE](./extensible-storage-engine-files.md)

Исходные файлы программы должны включать заголовочный файл ESENT. h для доступа к прототипам функций и определения структур для API-интерфейса расширенного подсистемы хранилища. Разработчики могут использовать файл библиотеки ESENT. lib для создания приложений, использующих API подсистемы расширенного хранилища. Во время выполнения приложения связываются с esent.dll.
