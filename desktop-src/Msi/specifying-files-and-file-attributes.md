---
description: установка и удаление каждого файла определяется компонентом установщик Windows, который управляет файлом.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Указание файлов и атрибутов файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdb63bf2779ddc5730013bad06b382c168a62bab5e897d5d621f7a65644e445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893734"
---
# <a name="specifying-files-and-file-attributes"></a>Указание файлов и атрибутов файлов

установка и удаление каждого файла определяется [компонентом установщик Windows](windows-installer-components.md) , который управляет файлом. После указания группировки ресурсов в компоненты сведения о атрибутах файла можно добавить в базу данных установки. в этом разделе вы добавите сведения о файле в базу данных установки для образца Блокнот. См. раздел [File Tables Group](file-tables-group.md).

файлы в образце Блокнот несжаты. Сведения о добавлении CAB-файлов в пакеты см. в разделе [сжатые и несжатые источники](compressed-and-uncompressed-sources.md) . Этот образец не содержит сведений об управлении версиями файлов. Дополнительные сведения об управлении версиями файлов см. в разделе [правила управления версиями](file-versioning-rules.md) файлов и [Управление версиями файлов по умолчанию](default-file-versioning.md).

Используйте редактор базы данных, чтобы открыть MNP2000.msi и ввести следующие данные в таблицу пустого файла.

[Таблица файлов](file-table.md)



| File         | Компонент\_ | FileName     | FileSize | Версия | Язык | Атрибуты | Последовательность |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Команды    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Концерт     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Dance       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Футбол    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Справка        | Help.txt     | 1000     |         |          | 0          | 1        |
| January.txt  | Январь     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | невеарс    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Блокнот     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Блокнот     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Продолжить](specifying-source-media.md)

 

 



