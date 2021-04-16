---
title: Функции Прожфс
description: Следующие функции объявляются в прожектедфслиб. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 40f3f2aec8e52d2caafdcf1554d0871e9bb185de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105719186"
---
# <a name="projfs-functions"></a>Функции Прожфс

Следующие функции объявляются в прожектедфслиб. h.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**пржаллокатеалигнедбуффер**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | Выделяет буфер, соответствующий требованиям к выравниванию памяти для устройства хранения экземпляра виртуализации. |
| [**пржклеарнегативепаскаче**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | Очищает кэш отрицательного пути экземпляра виртуализации, если он активен. |
| [**пржкомплетекомманд**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | Указывает, что поставщик завершил обработку обратного вызова, из которого он был ранее возвращен HRESULT_FROM_WIN32 (ERROR_IO_PENDING). |
| [**пржделетефиле**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | Позволяет поставщику удалить элемент, кэшированный в локальной файловой системе. |
| [**прждоеснамеконтаинвилдкардс**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | Определяет, содержит ли имя символы-шаблоны. |
| [**пржфиленамекомпаре**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | Сравнивает два имени файла и возвращает значение, указывающее порядок их относительных параметров сортировки. |
| [**пржфиленамематч**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | Определяет, соответствует ли имя файла шаблону поиска. |
| [**пржфиллдирентрибуффер**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | Предоставляет сведения для одного файла или каталога в перечисление. |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | Предоставляет сведения для одного файла или каталога в перечисление и позволяет вызывающему объекту указать расширенные сведения. |
| [**пржфриалигнедбуффер**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | Освобождает выделенный буфер. |
| [**пржжетондискфилестате**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | Возвращает состояние файла на диске для файла или каталога. |
| [**пржжетвиртуализатионинстанцеинфо**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | Извлекает сведения об экземпляре виртуализации. |
| [**пржмаркдиректорясплацехолдер**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | Преобразует существующий каталог в заполнитель каталога. |
| [**пржстартвиртуализинг**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | Настраивает экземпляр виртуализации Прожфс и запускает его, делая его доступным для обслуживания операций ввода-вывода и вызова обратных вызовов поставщика. |
| [**пржстопвиртуализинг**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | Останавливает выполняющийся экземпляр виртуализации Прожфс, делая его недоступным для службы ввода-вывода или включения обратных вызовов поставщика. |
| [**пржупдатефилеифнидед**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | Позволяет поставщику обновлять элемент, кэшированный в локальной файловой системе. |
| [**пржвритефиледата**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | Отправляет содержимое файла в Прожфс. |
| [**пржвритеплацехолдеринфо**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | Отправляет метаданные файла или каталога в Прожфс. |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | Отправляет метаданные файла или каталога в Прожфс и позволяет вызывающему объекту указать расширенные сведения. |
