---
description: Каждый раз, когда процесс создает или открывает объект каталога, он получает обработчик для объекта.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Дескрипторы каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664605"
---
# <a name="directory-handles"></a>Дескрипторы каталогов

Каждый раз, когда процесс создает или открывает объект каталога, он получает обработчик для объекта.

Чтобы получить маркер существующего каталога, вызовите функцию [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) с флагом **File \_ Flag \_ \_ семантики резервного копирования** .

Вы можете передать маркер каталога следующим функциям.



| Функция                                                         | Описание                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**баккупреад**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | Создайте резервную копию файла или каталога, включая сведения о безопасности.<br/>                                                                                      |
| [**баккупсик**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | Поиск вперед в потоке данных, доступ к которому осуществляется с помощью функции [**баккупреад**](/windows/desktop/api/winbase/nf-winbase-backupread) или [**баккупврите**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .<br/> |
| [**баккупврите**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | Восстановление файла или каталога, резервная копия которых была создана с помощью [**баккупреад**](/windows/desktop/api/winbase/nf-winbase-backupread).<br/>                                                             |
| [**жетфилеинформатионбихандле**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | Возвращает сведения о файле для указанного файла.<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | Возвращает размер указанного файла в байтах.<br/>                                                                                                   |
| [**Функции getFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Извлекает дату и время создания файла или каталога, последнего доступа и последнего изменения.<br/>                                                   |
| [**жетфилетипе**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | Возвращает тип файла указанного файла.<br/>                                                                                                        |
| [**реаддиректоричанжесв**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | Извлекает сведения, описывающие изменения в указанном каталоге.<br/>                                                                      |
| [**сетфилетиме**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Задает дату и время создания указанного файла или каталога, последнего доступа или последнего изменения.<br/>                                             |



 

 

