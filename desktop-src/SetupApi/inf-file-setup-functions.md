---
description: Следующие функции API установки используются с INF-файлами.
ms.assetid: fb4263fc-5f59-460a-a7d9-93f10729c02a
title: Функции установки INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24944f19938217d40ff4a7eaebbfb638c26e4afb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663907"
---
# <a name="inf-file-setup-functions"></a>Функции установки INF-файла

Следующие функции API установки используются с INF-файлами.



| Функция                                                                         | Описание                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**сетупклосеинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)                                   | Освобождает ресурсы и закрывает INF-файл.                                                                                                                                                             |
| [**сетупдекомпрессоркопифиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)                   | Копирует файл и, при необходимости, распаковывает его.                                                                                                                                                      |
| [**сетупфиндфирстлине**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                                 | Находит первую строку в разделе INF-файла или, если указан ключ, первая строка, соответствующая этому ключу. Обновляет элемент **строки** структуры [**инфконтекст**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) . |
| [**сетупфинднекстлине**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                                   | Возвращает следующую строку в разделе относительно элемента **строки** указанной структуры [**инфконтекст**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) .                                                                    |
| [**сетупфинднекстматчлине**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                         | Возвращает следующую строку в разделе относительно элемента **строки** указанного [**инфконтекст**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) , соответствующего указанному ключу.                                                 |
| [**сетупжетбинарифиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                               | Извлекает данные из строки, поля которой находятся в двоичном формате.                                                                                                                                          |
| [**сетупжетфиелдкаунт**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)                                 | Возвращает число полей в строке.                                                                                                                                                                |
| [**сетупжетфилекомпрессионинфо**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)               | Получает сведения о сжатии файлов из INF-файла.                                                                                                                                               |
| [**сетупжетинффилелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)                               | Возвращает список типов INF-файлов в указанном каталоге.                                                                                                                                        |
| [**сетупжетинфинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                         | Возвращает сведения об INF-файле (членом **строки** [**инфконтекст**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) или filename).                                                                                     |
| [**сетупжетинтфиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                     | Возвращает указанное целочисленное поле строки в INF-файле.                                                                                                                                          |
| [**сетупжетлинебиндекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                               | Обновляет элемент **строки** [**инфконтекст**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) для строки по указанному индексу в указанном разделе.                                                                     |
| [**сетупжетлинекаунт**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)                                   | Возвращает количество строк в указанном разделе.                                                                                                                                                  |
| [**сетупжетлинетекст**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                     | Извлекает содержимое указанной строки из INF-файла.                                                                                                                                            |
| [**сетупжетмултисзфиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                             | Возвращает список строк, начиная с указанного поля строки в INF-файле.                                                                                                                   |
| [**сетупжетсаурцефилелокатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)                 | Возвращает порядковый номер и путь к исходному диску (относительно корневого каталога источника), где находится исходный файл.                                                                                                       |
| [**сетупжетсаурцефилесизе**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                         | Возвращает размер файла для отдельного исходного файла или раздела **копирования файлов** INF-файла.                                                                                                           |
| [**сетупжетсаурцеинфо**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                                 | Извлекает путь, файл тегов или описание источника.                                                                                                                                             |
| [**сетупжетстрингфиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                               | Возвращает указанное строковое поле строки в INF-файле.                                                                                                                                           |
| [**сетупжеттаржетпас**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                                 | Получает целевой путь для раздела **копирования файлов** в INF-файле.                                                                                                                                      |
| [**сетупинсталлфиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)                                     | Устанавливает файл.                                                                                                                                                                                       |
| [**сетупинсталлфиликс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)                                 | Устанавливает файл и возвращает переменную, указывающую, используется ли файл.                                                                                                                  |
| [**сетупинсталлфилесфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)       | Ставит в очередь все файлы, указанные в разделах " **Копировать файлы**", " **удалить файлы**" и " **Переименовать файлы** ", которые перечислены в разделе " **Установка** ".                                                       |
| [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)                 | Выполняет директивы, указанные в разделе **установки** INF-файла.                                                                                                                                  |
| [**сетупинсталлсервицесфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) | Выполняет операции установки и удаления службы, как указано в разделе **службы** INF-файла.                                                                                            |
| [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)                         | Открывает INF-файл и добавляет его к существующему INF-файлу.                                                                                                                                             |
| [**сетупопенинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)                                     | Открывает INF-файл и возвращает к нему маркер.                                                                                                                                                          |
| [**сетупопенмастеринф**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)                                 | Открывает INF-файл, содержащий сведения о файле и макете для файлов, поставляющихся с системой.                                                                                                        |
| [**сетупкуеринффилеинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)             | Запрашивает информационную структуру INF о связанных с ней именах файлов INF.                                                                                                                               |
| [**сетупкуеринфверсионинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)       | Запрашивает структуру данных INF для получения сведений о версии одного из его составляющих INF-файлов.                                                                                                      |
| [**сетупсетдиректорид**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)                               | Связывает новый идентификатор каталога с определенным каталогом.                                                                                                                                     |



 

 

 



