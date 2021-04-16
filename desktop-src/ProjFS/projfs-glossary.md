---
title: Глоссарий файловой системы Windows
description: Специальные термины, используемые в Прожфс.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/21/2020
ms.locfileid: "105719113"
---
# <a name="windows-projected-file-system-glossary"></a>Глоссарий файловой системы Windows

Специальные термины, используемые в Прожфс.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**Резервное хранилище**
</dt>
<dd>

Иерархические данные, поддерживаемые поставщиком, которые проецируются в файловую систему как файлы и каталоги.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**заполнитель "грязный"**
</dt>
<dd>

Файл или каталог, который был локально изменен и больше не является кэшем своего состояния в хранилище поставщика.  См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**полный файл или каталог**
</dt>
<dd>

Файл или каталог, созданный в локальной файловой системе, или файл, который был изменен, что делает его недоступным для кэша своего состояния в резервном хранилище.  См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**заполнитель заархивированного текста**
</dt>
<dd>

Файл, содержимое и метаданные которого были кэшированы на диск.  См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**заполнителе**
</dt>
<dd>

Файл или каталог, который не полностью указан на диске.  См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**отметки полного удаления**
</dt>
<dd>

Специальный скрытый заполнитель, представляющий элемент, который был удален из локальной файловой системы.  См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**виртуальный файл или каталог**
</dt>
<dd>

Файл или каталог, который физически не существует на диске, но проецируется на результаты перечисления.  См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**экземпляр виртуализации**
</dt>
<dd>

Объект в памяти, который управляет взаимодействием между поставщиком и Прожфс для набора файлов и каталогов, расположенных в определенном корне виртуализации.
</dd>

<dt>

<span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**корень виртуализации**
</dt>
<dd>

Каталог в файловой системе, в которой проецируется данные поставщика.
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->