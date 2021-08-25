---
description: Функции, используемые для управления подключенными папками.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Функции подключенных папок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13175dc4846d8f8438a3f1b94b3e407aaf347e2b6d10ad5c3761899882ecdfaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870784"
---
# <a name="mounted-folder-functions"></a>Функции подключенных папок

Функции подключенных папок можно разделить на три группы: функции общего назначения, функции, используемые для проверки томов, и функции, используемые для сканирования тома для подключенных папок.

## <a name="general-purpose-mounted-folder-functions"></a>General-Purpose функции подключенных папок



| Функция                                                                     | Описание                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**делетеволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Удаляет букву диска или подключенную папку.                                                                                                                   |
| [**жетволуменамефорволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Получение пути GUID тома, связанного с указанной точкой подключения тома (буква диска, путь GUID тома или подключенная папка). |
| [**жетволумепаснаме**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Извлекает подключенную папку, связанную с указанным томом.                                                                                  |
| [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Связывает том с буквой диска или каталогом на другом томе.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Функции Volume-Scanning



| Функция                                   | Описание                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Возвращает имя тома на компьютере. [**Финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) используется для начала перечисления томов компьютера. |
| [**финднекстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Возобновляет поиск тома, запущенный с помощью вызова [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).                                                     |
| [**финдволумеклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Закрывает Поиск томов.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Функции сканирования подключенных папок



| Функция                                                       | Описание                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Извлекает имя подключенной папки на указанном томе. [**Финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) используется для начала сканирования подключенных папок на томе. |
| [**финднекстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Возобновляет поиск подключенных папок, начатый вызовом [**финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).                                                                    |
| [**финдволумемаунтпоинтклосе**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Закрывает поиск подключенных папок.                                                                                                                                                      |



 

 

 



