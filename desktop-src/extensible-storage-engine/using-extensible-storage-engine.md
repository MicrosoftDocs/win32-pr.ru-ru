---
description: 'дополнительные сведения о: использование расширяемого механизма служба хранилища'
title: использование расширяемого механизма служба хранилища
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e994b423b56b092e8865ad2440829aecfe3832b5a36d015869e0b700c2579a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118070444"
---
# <a name="using-extensible-storage-engine"></a>использование расширяемого механизма служба хранилища


_**Применимо к:** Windows | Windows Сервером_

## <a name="using-extensible-storage-engine"></a>использование расширяемого механизма служба хранилища

В этом разделе содержатся общие сведения об использовании следующих частей API ESE.

  - [Столбцы](./columns.md)

  - [Индексирование в таблице](./indexing-in-the-table.md)

  - [Создание баз данных](./creating-databases.md)

  - [Транзакции](./transactions.md)

  - [Ошибки ESE](./extensible-storage-engine-errors.md)

  - [Файлы ESE](./extensible-storage-engine-files.md)

исходные файлы программы должны включать файл заголовка esent. h для доступа к прототипам функций и определения структур для расширяемого API-интерфейса служба хранилища Engine. разработчики могут использовать файл библиотеки esent. lib для создания приложений, использующих API-интерфейс расширенного обработчика служба хранилища. Во время выполнения приложения связываются с esent.dll.
