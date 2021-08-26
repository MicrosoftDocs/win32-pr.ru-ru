---
description: Функции, используемые в управлении томами.
ms.assetid: dc985126-970c-49f2-877f-3759125e43b6
title: Функции управления томами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3673e73007c977992d0209bcd79ded2afd4ed555ec3a22821e5f74d90e3cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130694"
---
# <a name="volume-management-functions"></a>Функции управления томами

Функции, используемые в управлении томами.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                   | Описание                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**дефинедосдевице**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew)<br/>                                   | Определяет, переопределяет или удаляет имена устройств MS-DOS.<br/>                                                                                                                |
| [**делетеволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)<br/>                     | Удаляет букву диска или подключенную папку.<br/>                                                                                                                          |
| [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)<br/>                                   | Возвращает имя тома на компьютере. <br/>                                                                                                                     |
| [**финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)<br/>               | Извлекает имя подключенной папки на указанном томе. <br/>                                                                                                   |
| [**финднекстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)<br/>                                     | Возобновляет поиск тома, запущенный вызовом функции [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) . <br/>                                                           |
| [**финднекстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)<br/>                 | Возобновляет поиск подключенных папок, начатый вызовом функции [**финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) . <br/>                               |
| [**финдволумеклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)<br/>                                   | Закрывает указанный маркер поиска тома.<br/>                                                                                                                         |
| [**финдволумемаунтпоинтклосе**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)<br/>               | Закрывает указанный обработчик поиска подключенных папок.<br/>                                                                                                                 |
| [**жетдриветипе**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea)<br/>                                         | Определяет, является ли диск съемным, фиксированным, КОМПАКТным, ОПЕРАТИВным или сетевым диском.<br/>                                                                         |
| [**жетлогикалдривес**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives)<br/>                                 | Извлекает битовую маску, представляющую доступные в данный момент диски.<br/>                                                                                              |
| [**жетлогикалдривестрингс**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)<br/>                     | Заполняет буфер строками, задающих допустимые диски в системе.<br/>                                                                                               |
| [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                         | Извлекает сведения о файловой системе и томе, связанные с указанным корневым каталогом.<br/>                                                               |
| [**жетволумеинформатионбихандлев**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationbyhandlew)<br/>       | Извлекает сведения о файловой системе и томе, связанные с указанным файлом.<br/>                                                                         |
| [**жетволуменамефорволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)<br/> | Извлекает путь **GUID** тома, связанный с указанной точкой подключения тома (буква диска, путь **GUID** тома или подключенная папка).<br/> |
| [**жетволумепаснаме**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)<br/>                               | Возвращает точку подключения тома, в которой подключен указанный путь.<br/>                                                                                              |
| [**жетволумепаснамесфорволуменаме**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)<br/>   | Возвращает список букв диска и пути к подключенной папке для указанного тома.<br/>                                                                               |
| [**куеридосдевице**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)<br/>                                     | Извлекает сведения об именах устройств MS-DOS.<br/>                                                                                                                   |
| [**сетволумелабел**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)<br/>                                     | Задает метку тома файловой системы.<br/>                                                                                                                            |
| [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)<br/>                           | Связывает том с буквой диска или каталогом на другом томе.<br/>                                                                                          |



 

Следующие функции используются с точками подключения томов (буквы дисков, пути GUID томов и подключенные папки).

-   [**делетеволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)
-   [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**финднекстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**финднекстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**финдволумеклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)
-   [**финдволумемаунтпоинтклосе**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)
-   [**жетволуменамефорволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)
-   [**жетволумепаснаме**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)
-   [**жетволумепаснамесфорволуменаме**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)
-   [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)

 

 




