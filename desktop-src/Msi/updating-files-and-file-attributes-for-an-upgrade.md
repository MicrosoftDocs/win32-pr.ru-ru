---
description: Так как обновление обновляет файлы, используемые приложением, необходимо изменить таблицу файлов базы данных.
ms.assetid: 65a7ae86-b426-4dd4-8cf5-f905dc2a1727
title: Обновление файлов и атрибутов файлов для обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c56560432a18746b31e3bb983be1f465199c51b15601c3dfd47911fe7f6ab4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809894"
---
# <a name="updating-files-and-file-attributes-for-an-upgrade"></a>Обновление файлов и атрибутов файлов для обновления

Так как обновление обновляет файлы, используемые приложением, необходимо изменить [таблицу файлов](file-table.md) базы данных. Используйте редактор базы данных Orca, поставляемый с пакетом SDK, или другой редактор, чтобы открыть MNP2001.msi и ввести в [таблицу файлов](file-table.md)следующие данные.

[Таблица файлов](file-table.md)



| File         | Компонент\_ | FileName     | FileSize | Версия | Язык | Атрибуты | Последовательность |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseba01.txt | Команды    | Baseba01.txt | 1000     |         |          | 0          | 1        |
| Concer01.txt | Концерт     | Concer01.txt | 1000     |         |          | 0          | 1        |
| Dance01.txt  | Dance       | Dance01.txt  | 1000     |         |          | 0          | 1        |
| Opera01.txt  | Opera       | Opera01.txt  | 1000     |         |          | 0          | 1        |
| Footba01.txt | Футбол    | Footba01.txt | 1000     |         |          | 0          | 1        |
| Basket01.txt | Баскетбол  | Basket01.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Справка        | Help.txt     | 1000     |         |          | 0          | 1        |
| Januar01.txt | Январь     | Januar01.txt | 1000     |         |          | 0          | 1        |
| NewYea01.txt | невеарс    | NewYea01.txt | 1000     |         |          | 0          | 1        |
| Memori01.txt | мемориал    | Memori01.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Блокнот     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Блокнот     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Продолжить](updating-components-for-an-upgrade.md)

 

 



