---
description: В списке дискового пространства используются следующие функции.
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Функции списка Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f520cc7a3ddcd0b12b27bd11768a95231a8ed4b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346515"
---
# <a name="disk-space-list-functions"></a>Функции списка Disk-Space

В списке дискового пространства используются следующие функции.



| Функция                                                                                         | Описание                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**сетупаджустдискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | Корректирует объем необходимого пространства для указанного диска.                                                                          |
| [**сетупкреатедискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | Создает список дискового пространства и выделяет ему ресурсы.                                                                             |
| [**сетупдестройдискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | Уничтожает список дискового пространства, освобождая ресурсы, выделенные для него.                                                                   |
| [**сетупдупликатедискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | Дублирует список дискового пространства как новый независимый список дискового пространства.                                                                   |
| [**сетупкуеридривесиндискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | Заполняет буфер спецификациями диска для всех дисков, перечисленных в списке дискового пространства.                                       |
| [**сетупкуериспацерекуиредондриве**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | Возвращает общий объем дискового пространства, необходимого для завершения операций с файлами на определенном диске, указанном в списке дискового пространства. |
| [**сетупаддтодискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | Добавляет операцию копирования или удаления файла в список дискового пространства.                                                                         |
| [**сетупаддсектионтодискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | Добавляет все операции с файлами в раздел **копирование файлов** или **Удаление файлов** INF-файла в список дискового пространства.                    |
| [**сетупаддинсталлсектионтодискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | Добавляет все операции с файлами в раздел **установки** INF-файла в список дискового пространства.                                        |
| [**сетупремовефромдискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | Удаляет операцию копирования или удаления файла из списка дискового пространства.                                                                      |
| [**сетупремовесектионфромдискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | Удаляет все операции с файлами в разделе **копирование файлов** или **Удаление файлов** INF-файла из списка дискового пространства.               |
| [**сетупремовеинсталлсектионфромдискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | Удаляет все операции с файлами из раздела **Установка** INF-файла из списка дискового пространства.                                  |



 

 

 



