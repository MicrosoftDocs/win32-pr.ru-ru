---
description: 'Дополнительные сведения: методы API'
title: Методы API
TOCTitle: Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api_methods(v=EXCHG.10)
ms:contentKeyID: 55100697
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 75a2c7e81952b7afdbb73eb75228314f8ae3c77a35329626975fc6f5b03dee8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272832"
---
# <a name="api-methods"></a>Методы API

Включить защищенные члены  
Включить унаследованные члены  

Тип [API](./api-class.md) предоставляет следующие члены.

## <a name="methods"></a>Методы

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292138(v=exchg.10).md">Десериализеобжектфромколумн (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Десериализация объекта из столбца.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292115(v=exchg.10).md">Десериализеобжектфромколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Десериализация объекта из столбца.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292114(v=exchg.10).md">ескровупдате</a></td>
<td>Выполнить атомарное сложение для одного столбца. Столбец должен иметь тип <a href="hh577895(v=exchg.10).md">Long</a>. Эта функция позволяет нескольким сеансам одновременно обновлять одну и ту же запись без конфликтов.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292099(v=exchg.10).md">Выкладка</a></td>
<td>Извлекает закладку для записи, связанной с элементом индекса, в текущем положении курсора. Эту закладку можно использовать для перемещения курсора обратно в ту же запись с помощью Жетготобукмарк.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292098(v=exchg.10).md">жетколумндиктионари</a></td>
<td>Создает словарь, который сопоставляет имена столбцов с их идентификаторами столбцов.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292101(v=exchg.10).md">жеттаблеколумнид</a></td>
<td>Получение columnid указанного столбца.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292090(v=exchg.10).md">Жеттаблеколумнс (JET_SESID, JET_TABLEID)</a></td>
<td>Выполняет перебор всех столбцов в таблице, возвращая сведения о каждом из них.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292089(v=exchg.10).md">Жеттаблеколумнс (JET_SESID, JET_DBID, строка)</a></td>
<td>Выполняет перебор всех столбцов в таблице, возвращая сведения о каждом из них.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292093(v=exchg.10).md">Жеттаблеиндексес (JET_SESID, JET_TABLEID)</a></td>
<td>Выполняет перебор всех индексов в таблице, возвращая сведения о каждой из них.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292092(v=exchg.10).md">Жеттаблеиндексес (JET_SESID, JET_DBID, строка)</a></td>
<td>Выполняет перебор всех индексов в таблице, возвращая сведения о каждой из них.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292095(v=exchg.10).md">Выtablename</a></td>
<td>Возвращает имена таблиц в базе данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292094(v=exchg.10).md">интерсектиндексес</a></td>
<td>Пересекает группу диапазонов индексов и возвращает закладки записей, которые находятся во всех диапазонах индекса. См. также <a href="dn292212(v=exchg.10).md">жетинтерсектиндексес (JET_SESID, [], Int32, JET_RECORDLIST, интерсектиндексесгрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292097(v=exchg.10).md">жетаддколумн</a></td>
<td>Добавить новый столбец в существующую таблицу.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292096(v=exchg.10).md">жетаттачдатабасе</a></td>
<td>Присоединяет файл базы данных для использования с экземпляром базы данных. Чтобы использовать базу данных, ее потребуется впоследствии открыть с помощью <a href="dn292219(v=exchg.10).md">жетопендатабасе (JET_SESID, String, String, JET_DBID, опендатабасегрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></td>
<td>Присоединяет файл базы данных для использования с экземпляром базы данных. Чтобы использовать базу данных, ее потребуется впоследствии открыть с помощью <a href="dn292219(v=exchg.10).md">жетопендатабасе (JET_SESID, String, String, JET_DBID, опендатабасегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292102(v=exchg.10).md">жетбаккупинстанце</a></td>
<td>Выполняет потоковую архивацию экземпляра, включая все подключенные базы данных, в каталог. При наличии нескольких методов резервного копирования, поддерживаемых ядром, это самая простая и наиболее Инкапсулированная функция.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292104(v=exchg.10).md">жетбегинекстерналбаккупинстанце</a></td>
<td>Инициирует внешнюю архивацию, пока ядро и база данных находятся в сети и активны.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292103(v=exchg.10).md">жетбегинсессион</a></td>
<td>Инициализируйте новый сеанс ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292105(v=exchg.10).md">жетбегинтрансактион</a></td>
<td>Заставляет сеанс войти в транзакцию или создать новую точку сохранения в существующей транзакции.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></td>
<td>Заставляет сеанс войти в транзакцию или создать новую точку сохранения в существующей транзакции.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292107(v=exchg.10).md">жетклоседатабасе</a></td>
<td>Закрывает файл базы данных, который был ранее открыт с помощью <a href="dn292219(v=exchg.10).md">жетопендатабасе (JET_SESID, String, String, JET_DBID, опендатабасегрбит)</a> или создается с помощью <a href="dn292118(v=exchg.10).md">жеткреатедатабасе (JET_SESID, String, String, JET_DBID, креатедатабасегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292108(v=exchg.10).md">жетклосефилеинстанце</a></td>
<td>Закрывает файл, Открытый с помощью Жетопенфилеинстанце после извлечения данных из этого файла с помощью Жетреадфилеинстанце.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292109(v=exchg.10).md">жетклосетабле</a></td>
<td>Закройте открытую таблицу.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292110(v=exchg.10).md">жеткоммиттрансактион</a></td>
<td>Фиксирует изменения, внесенные в состояние базы данных во время текущей точки сохранения, и переносит их в предыдущую точку сохранения. При фиксации самой внешней точки сохранения изменения, внесенные во время этой точки сохранения, будут зафиксированы в состоянии базы данных, и сеанс завершит транзакцию.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292112(v=exchg.10).md">жеткомпакт</a></td>
<td>Создает копию существующей базы данных. Копия сжимается в состояние, оптимальное для использования. Данные в скопированных данных будут упаковываться в соответствии с мерами, выбранными для индексов при создании индекса. Таким образом, сжатые данные могут храниться как можно более плотно. Кроме того, сжатые данные могут резервировать пространство для последующего роста записи или вставки индекса.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292113(v=exchg.10).md">жеткомпутестатс</a></td>
<td>Просматривает каждый индекс таблицы, чтобы точно вычислить количество записей в индексе и количество различных ключей в индексе. Эти сведения вместе с количеством страниц базы данных, выделенных для индекса, и текущим временем вычислений хранятся в метаданных индекса в базе данных. Эти данные можно впоследствии извлечь с помощью информационных операций.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292118(v=exchg.10).md">жеткреатедатабасе</a></td>
<td>Создает и прикрепляет файл базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></td>
<td>Создает и прикрепляет файл базы данных с указанным максимальным размером базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292121(v=exchg.10).md">жеткреатеиндекс</a></td>
<td>Создает индекс для данных в базе данных ESE. Индекс можно использовать для быстрого выявления конкретных данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></td>
<td>Создает индексы для данных в базе данных ESE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292122(v=exchg.10).md">жеткреатеинстанце</a></td>
<td>Выделяет новый экземпляр ядра СУБД.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></td>
<td>Выделение нового экземпляра ядра СУБД для использования в одном процессе с указанным отображаемым именем.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292127(v=exchg.10).md">жеткреатетабле</a></td>
<td>Создайте пустую таблицу. Вновь созданная таблица открывается исключительно.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></td>
<td>Создает таблицу, добавляет столбцы и индексы для этой таблицы.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292130(v=exchg.10).md">жетдефрагмент</a></td>
<td>Запускает и останавливает задачи дефрагментации базы данных, которые улучшают организацию данных в базе данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292145(v=exchg.10).md">JetDefragment2</a></td>
<td>Запускает и останавливает задачи дефрагментации базы данных, которые улучшают организацию данных в базе данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292131(v=exchg.10).md">жетделете</a></td>
<td>Удаляет текущую запись в таблице базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292133(v=exchg.10).md">жетделетеколумн</a></td>
<td>Удаляет столбец из таблицы базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></td>
<td>Удаляет столбец из таблицы базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292135(v=exchg.10).md">жетделетеиндекс</a></td>
<td>Удаляет индекс из таблицы базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292134(v=exchg.10).md">жетделететабле</a></td>
<td>Удаляет таблицу из базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292139(v=exchg.10).md">жетдетачдатабасе</a></td>
<td>Освобождает файл базы данных, который был ранее присоединен к сеансу базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></td>
<td>Освобождает файл базы данных, который был ранее присоединен к сеансу базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292137(v=exchg.10).md">жетдупкурсор</a></td>
<td>Дублирует открытый курсор и возвращает указатель на дублирующийся курсор. Если курсор, который был продублирован, был курсором только для чтения, то дубликат курсора также является курсором только для чтения. Любое состояние, связанное с построением ключа поиска или обновлением записи, не копируется в дублирующийся курсор. Кроме того, положение исходного курсора не дублируется в повторяющемся курсоре. Дубликат курсора всегда открывается в кластеризованном индексе, и его расположение всегда находится в первой строке таблицы.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292140(v=exchg.10).md">жетдупсессион</a></td>
<td>Инициализируйте новый сеанс ESE в том же экземпляре, что и заданный сесид.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292142(v=exchg.10).md">жетендекстерналбаккупинстанце</a></td>
<td>Завершает сеанс внешнего резервного копирования. Этот API является последним в серии API-интерфейсов, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></td>
<td>Завершает сеанс внешнего резервного копирования. Этот API является последним в серии API-интерфейсов, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292144(v=exchg.10).md">жетендсессион</a></td>
<td>Завершает сеанс.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292148(v=exchg.10).md">жетенумератеколумнс</a></td>
<td>Эффективно извлекает набор столбцов и их значений из текущей записи курсора или буфера копирования этого курсора. Возвращаемые столбцы и значения могут быть ограничены списком идентификаторов столбцов, Итагсекуенце числами и другими характеристиками. Этот интерфейс API извлечения столбца уникален в том, что он возвращает сведения в динамически выделяемой памяти, получаемой с помощью предоставленного пользователем обратного вызова, совместимого с переопределением. Эта новая гибкость позволяет эффективно получать данные столбцов с определенными характеристиками (например, размер и количество элементов), неизвестных вызывающему объекту. Это устраняет необходимость использования режимов обнаружения Жетретриевеколумн для определения этих характеристик, чтобы настроить окончательный вызов Жетретриевеколумн, который будет успешно получать нужные данные.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292150(v=exchg.10).md">жетескровупдате</a></td>
<td>Выполняет атомарную операцию сложения для одного столбца. Эта функция позволяет нескольким сеансам одновременно обновлять одну и ту же запись без конфликтов. См. также <a href="dn292114(v=exchg.10).md">ескровупдате (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292147(v=exchg.10).md">жетфрибуффер</a></td>
<td>Освобождает память, выделенную при вызове ядра СУБД.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292154(v=exchg.10).md">жетжетаттачинфоинстанце</a></td>
<td>Используется во время резервного копирования, инициированного <a href="dn292104(v=exchg.10).md">жетбегинекстерналбаккупинстанце (JET_INSTANCE, бегинекстерналбаккупгрбит)</a> , для запроса экземпляров имен файлов базы данных, которые должны быть частью набора файлов резервной копии. Будут рассматриваться только те базы данных, которые в данный момент подключены к экземпляру с помощью <a href="dn292096(v=exchg.10).md">жетаттачдатабасе (JET_SESID, String, аттачдатабасегрбит)</a> . Эти файлы впоследствии могут быть открыты с помощью <a href="dn292230(v=exchg.10).md">жетопенфилеинстанце (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> и считаны с помощью <a href="dn332987(v=exchg.10).md">жетреадфилеинстанце (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292149(v=exchg.10).md">жетжетбукмарк</a></td>
<td>Извлекает закладку для записи, связанной с элементом индекса, в текущем положении курсора. Эта закладка может использоваться для перемещения курсора обратно в ту же запись с помощью <a href="dn292200(v=exchg.10).md">жетготобукмарк (JET_SESID, JET_TABLEID, [], Int32)</a>. Длина закладки не должна превышать <a href="dn351215(v=exchg.10).md">букмаркмост</a> байт. См. также <a href="dn292099(v=exchg.10).md">Закладка (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292158(v=exchg.10).md">Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNBASE)</a></td>
<td>Извлекает сведения о столбце в таблице.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292151(v=exchg.10).md">Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNDEF)</a></td>
<td>Извлекает сведения о столбце таблицы.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292152(v=exchg.10).md">Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNLIST)</a></td>
<td>Извлекает сведения обо всех столбцах в таблице.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292153(v=exchg.10).md">жетжеткуррентиндекс</a></td>
<td>Ддетерминес имя текущего индекса данного курсора. Это имя также используется для повторного выбора этого индекса в качестве текущего индекса с помощью <a href="dn334011(v=exchg.10).md">жетсеткуррентиндекс (JET_SESID, JET_TABLEID, String)</a>. Его также можно использовать для обнаружения свойств этого индекса с помощью Жетжеттаблеиндексинфо.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292155(v=exchg.10).md">жетжеткурсоринфо</a></td>
<td>Определить, будет ли обновление текущей записи курсора конфликтом записи в зависимости от текущего состояния обновления записи. Возможно, конфликт записи будет возвращен, даже если Жетжеткурсоринфо возвращается успешно. так как другой сеанс может обновить запись, прежде чем текущий сеанс сможет обновить ту же запись.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292159(v=exchg.10).md">Жетжетдатабасефилеинфо (строка, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Извлекает определенные сведения о заданной базе данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292161(v=exchg.10).md">Жетжетдатабасефилеинфо (String, Int32, JET_DbInfo)</a></td>
<td>Извлекает определенные сведения о заданной базе данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292160(v=exchg.10).md">Жетжетдатабасефилеинфо (String, Int64, JET_DbInfo)</a></td>
<td>Извлекает определенные сведения о заданной базе данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292162(v=exchg.10).md">Жетжетдатабасеинфо (JET_SESID, JET_DBID, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Извлекает определенные сведения о заданной базе данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292164(v=exchg.10).md">Жетжетдатабасеинфо (JET_SESID, JET_DBID, Int32, JET_DbInfo)</a></td>
<td>Извлекает определенные сведения о заданной базе данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292167(v=exchg.10).md">Жетжетдатабасеинфо (JET_SESID, JET_DBID, строка, JET_DbInfo)</a></td>
<td>Извлекает определенные сведения о заданной базе данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292168(v=exchg.10).md">Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST)</a></td>
<td><strong>Устарело.</strong> Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292172(v=exchg.10).md">Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292166(v=exchg.10).md">Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292171(v=exchg.10).md">Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, Int32, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292169(v=exchg.10).md">Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, строка, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292173(v=exchg.10).md">Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, UInt16, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292170(v=exchg.10).md">жетжетинстанцеинфо</a></td>
<td>Извлекает сведения о выполняемых экземплярах.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292175(v=exchg.10).md">жетжетлокк</a></td>
<td>Явно Зарезервируйте возможность обновления строки, блокировки записи или явного запрета обновления строки любым другим сеансом, блокировка чтения. Обычно блокировки записи строк получаются неявно в результате обновления строк. Блокировки чтения обычно не требуются из-за управления версиями записей. Однако в некоторых случаях транзакция может потребовать явно заблокировать строку для принудительного применения сериализации или убедиться, что дальнейшая операция будет выполнена.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292174(v=exchg.10).md">жетжетлогинфоинстанце</a></td>
<td>Используется во время резервного копирования, инициированного <a href="dn292104(v=exchg.10).md">жетбегинекстерналбаккупинстанце (JET_INSTANCE, бегинекстерналбаккупгрбит)</a> , чтобы запрашивать имена файлов исправления базы данных и журналов, которые должны стать частью набора файлов резервной копии. Эти файлы впоследствии могут быть открыты с помощью <a href="dn292230(v=exchg.10).md">жетопенфилеинстанце (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> и считаны с помощью <a href="dn332987(v=exchg.10).md">жетреадфилеинстанце (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292177(v=exchg.10).md">жетжетлс</a></td>
<td>позволяет приложению извлекать контекстный маркер, известный как локальный служба хранилища, связанный с курсором или с таблицей, связанной с этим курсором. Этот обработчик контекста должен быть ранее задан с помощью <a href="dn334015(v=exchg.10).md">жетсетлс (JET_SESID, JET_TABLEID, JET_LS, лсгрбит)</a>. Жетжетлс также можно использовать для одновременной выборки текущего контекста для курсора или таблицы и сброса дескриптора контекста.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292179(v=exchg.10).md">Жетжетобжектинфо (JET_SESID, JET_DBID, JET_OBJECTLIST)</a></td>
<td>Извлекает сведения об объектах базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292178(v=exchg.10).md">Жетжетобжектинфо (JET_SESID, JET_DBID, JET_objtyp, строка, JET_OBJECTINFO)</a></td>
<td>Извлекает сведения об объектах базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292181(v=exchg.10).md">жетжетрекордпоситион</a></td>
<td>Возвращает вертикальную точку текущей записи в текущем индексе в форме <a href="dn335256(v=exchg.10).md">JET_RECPOS</a> структуры. См. также раздел <a href="dn292207(v=exchg.10).md">жетготопоситион (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292180(v=exchg.10).md">жетжетсекондариндексбукмарк</a></td>
<td>Извлекает специальную закладку для записи вторичного индекса в текущем положении курсора. Эту закладку можно использовать для эффективного перемещения курсора обратно к той же записи индекса с помощью Жетготосекондариндексбукмарк. Это наиболее полезно при изменении расположения вторичного индекса, который содержит дублирующиеся ключи или содержит несколько записей индекса для одной и той же записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292182(v=exchg.10).md">Жетжетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</a></td>
<td>Возвращает параметры конфигурации базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292185(v=exchg.10).md">Жетжетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)</a></td>
<td>Возвращает параметры конфигурации базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292186(v=exchg.10).md">Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</a></td>
<td>Извлекает сведения о столбце таблицы.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292187(v=exchg.10).md">Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, строка, JET_COLUMNDEF)</a></td>
<td>Извлекает сведения о столбце таблицы.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292189(v=exchg.10).md">Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, строка, JET_COLUMNLIST)</a></td>
<td>Извлекает сведения обо всех столбцах в таблице.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292191(v=exchg.10).md">Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, строка, JET_INDEXLIST)</a></td>
<td><strong>Устарело.</strong> Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292190(v=exchg.10).md">Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, строка, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292196(v=exchg.10).md">Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, строка, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292193(v=exchg.10).md">Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292192(v=exchg.10).md">Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, строка, строка, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292195(v=exchg.10).md">Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</a></td>
<td>Извлекает сведения о индексах в таблице.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292197(v=exchg.10).md">Жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a></td>
<td>Извлекает различные фрагменты информации о таблице в базе данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292198(v=exchg.10).md">Жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a></td>
<td>Извлекает различные фрагменты информации о таблице в базе данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292201(v=exchg.10).md">Жетжеттаблеинфо (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a></td>
<td>Извлекает различные фрагменты информации о таблице в базе данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292202(v=exchg.10).md">Жетжеттаблеинфо (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a></td>
<td>Извлекает различные фрагменты информации о таблице в базе данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292204(v=exchg.10).md">Жетжеттаблеинфо (JET_SESID, JET_TABLEID, строка, JET_TblInfo)</a></td>
<td>Извлекает различные фрагменты информации о таблице в базе данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292199(v=exchg.10).md">жетжеттрункателогинфоинстанце</a></td>
<td>Используется во время резервного копирования, инициированного <a href="dn292104(v=exchg.10).md">жетбегинекстерналбаккупинстанце (JET_INSTANCE, бегинекстерналбаккупгрбит)</a> , чтобы запросить у экземпляра имена файлов журнала транзакций, которые можно безопасно удалить после успешного завершения резервного копирования.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292203(v=exchg.10).md">жетжетверсион</a></td>
<td>Извлекает версию ядра СУБД.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292200(v=exchg.10).md">жетготобукмарк</a></td>
<td>Позиционирует курсор на запись индекса для записи, связанной с указанной закладкой. Закладку можно использовать с любым индексом, определенным для таблицы. Закладку для записи можно получить с помощью <a href="dn292149(v=exchg.10).md">жетжетбукмарк (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292207(v=exchg.10).md">жетготопоситион</a></td>
<td>Перемещает курсор на новое место, которое представляет собой часть пути с помощью текущего индекса. См. также раздел <a href="dn292181(v=exchg.10).md">жетжетрекордпоситион (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292205(v=exchg.10).md">жетготосекондариндексбукмарк</a></td>
<td>Позиционирует курсор на запись индекса, связанную с закладкой дополнительного индекса. Закладку вторичного индекса необходимо использовать с тем же индексом для той же таблицы, из которой она была первоначально извлечена. Закладку вторичного индекса для записи индекса можно получить с помощью <a href="dn292205(v=exchg.10).md">жетготосекондариндексбукмарк (JET_SESID, JET_TABLEID, [], Int32, [], Int32, готосекондариндексбукмаркгрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292206(v=exchg.10).md">жетгровдатабасе</a></td>
<td>Увеличивает размер открытой в данный момент базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292208(v=exchg.10).md">жетидле</a></td>
<td>Выполняет задачи очистки при простое или проверяет состояние хранилища версий в ESE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292209(v=exchg.10).md">жетиндексрекордкаунт</a></td>
<td>Подсчитывает количество записей в текущем индексе до текущей позиции вперед. Текущая позицией включается в число. Число может быть больше, чем общее число записей в таблице, если текущий индекс находится над многозначным столбцом, а экземпляры столбца имеют несколько значений. Если таблица пуста, для счетчика будет возвращено значение 0.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292210(v=exchg.10).md">жетинит</a></td>
<td>Инициализируйте ядро СУБД ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292214(v=exchg.10).md">JetInit2</a></td>
<td>Инициализируйте ядро СУБД ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292212(v=exchg.10).md">жетинтерсектиндексес</a></td>
<td>Выполняет пересечение нескольких наборов записей индекса из разных вторичных индексов по той же таблице. Эта операция полезна для поиска набора записей в таблице, соответствующих двум или более критериям, которые могут быть выражены с помощью диапазонов индексов. См. также <a href="dn292094(v=exchg.10).md">интерсектиндексес (JET_SESID, [])</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292216(v=exchg.10).md">жетмакекэй</a></td>
<td>Конструирует ключи поиска, которые затем могут использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292218(v=exchg.10).md">Жетмове (JET_SESID, JET_TABLEID, JET_Move, Мовегрбит)</a></td>
<td>Навигация по индексу. Курсор может располагаться в начале или в конце индекса и перемещаться назад и вперед по заданному числу записей индекса. См. также <a href="dn334150(v=exchg.10).md">тримовефирст (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">тримовеласт (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">тримовенекст (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">тримовепревиаус (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292217(v=exchg.10).md">Жетмове (JET_SESID, JET_TABLEID, Int32, Мовегрбит)</a></td>
<td>Навигация по индексу. Курсор может располагаться в начале или в конце индекса и перемещаться назад и вперед по заданному числу записей индекса. См. также <a href="dn334150(v=exchg.10).md">тримовефирст (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">тримовеласт (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">тримовенекст (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">тримовепревиаус (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292219(v=exchg.10).md">жетопендатабасе</a></td>
<td>Открывает базу данных, ранее присоединенную с помощью <a href="dn292096(v=exchg.10).md">жетаттачдатабасе (JET_SESID, String, аттачдатабасегрбит)</a>, для использования с сеансом базы данных. Эту функцию можно вызывать несколько раз для одной и той же базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292230(v=exchg.10).md">жетопенфилеинстанце</a></td>
<td>Открывает присоединенную базу данных, файл исправления базы данных или файл журнала транзакций активного экземпляра с целью выполнения потоковой архивации нечеткого резервного копирования. Затем данные из этих файлов можно считать с помощью возвращенного маркера с помощью Жетреадфилеинстанце. Возвращаемый обработчик должен быть закрыт с помощью Жетклосефилеинстанце. Внешнее резервное копирование экземпляра должно быть ранее инициировано с помощью Жетбегинекстерналбаккупинстанце.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292234(v=exchg.10).md">жетопентабле</a></td>
<td>Открывает курсор для ранее созданной таблицы.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292231(v=exchg.10).md">жетопентемптабле</a></td>
<td>Создает временную таблицу с одним индексом. Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс. Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером. Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно. См. также <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">Жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></td>
<td>Создает временную таблицу с одним индексом. Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс. Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером. Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно. См. также <a href="dn292231(v=exchg.10).md">жетопентемптабле (JET_SESID, [], Int32, темптаблегрбит, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">Жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></td>
<td>Создает временную таблицу с одним индексом. Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс. Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером. Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно. См. также <a href="dn292231(v=exchg.10).md">жетопентемптабле (JET_SESID, [], Int32, темптаблегрбит, JET_TABLEID, [])</a>, <a href="dn335326(v=exchg.10).md">жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332998(v=exchg.10).md">жетосснапшотфризе</a></td>
<td>Запускает моментальный снимок. Во время выполнения моментального снимка подсистема не может выполнить действия записи на диск.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn292235(v=exchg.10).md">жетосснапшотпрепаре</a></td>
<td>Начинает подготовку сеанса моментального снимка. Сеанс моментальных снимков — это короткий интервал времени, в течение которого модуль не выполняет никаких операций записи с диска IOs на диск, чтобы подсистема могла участвовать в сеансе моментальных снимков тома (при использовании модуля записи моментальных снимков).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332986(v=exchg.10).md">жетосснапшотсав</a></td>
<td>Уведомляет ядро о возможности возобновления обычных операций ввода-вывода после точки фиксации и успешного создания моментального снимка.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332988(v=exchg.10).md">жетпрепареупдате</a></td>
<td>Подготовка курсора к обновлению.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332987(v=exchg.10).md">жетреадфилеинстанце</a></td>
<td>Извлекает содержимое файла, открытого с помощью <a href="dn292230(v=exchg.10).md">жетопенфилеинстанце (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332989(v=exchg.10).md">жетрегистеркаллбакк</a></td>
<td>Позволяет приложению настроить ядро СУБД на выдачу уведомлений для конкретных событий в приложении. Эти уведомления связаны с определенной таблицей и остаются в силе только до тех пор, пока экземпляр, содержащий таблицу, не завершит работу с помощью <a href="dn334020(v=exchg.10).md">жеттерм (JET_INSTANCE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332990(v=exchg.10).md">жетренамеколумн</a></td>
<td>Изменяет имя существующего столбца.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332993(v=exchg.10).md">жетренаметабле</a></td>
<td>Изменяет имя существующей таблицы.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332991(v=exchg.10).md">жетресетсессионконтекст</a></td>
<td>Отменяет связь сеанса с текущим потоком. Его следует использовать вместе с <a href="dn334027(v=exchg.10).md">жетсетсессионконтекст (JET_SESID, IntPtr)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332994(v=exchg.10).md">жетресеттаблесекуентиал</a></td>
<td>Уведомляет ядро СУБД о том, что приложение больше не просматривает весь индекс, на котором расположен курсор. Этот вызов обращается к отправке уведомления, отправленного <a href="dn334018(v=exchg.10).md">жетсеттаблесекуентиал (JET_SESID, JET_TABLEID, сеттаблесекуентиалгрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332992(v=exchg.10).md">жетрестореинстанце</a></td>
<td>Восстанавливает и восстанавливает потоковую передачу резервной копии экземпляра, включая все подключенные базы данных. Он предназначен для работы с резервной копией, созданной с помощью функции <a href="dn292102(v=exchg.10).md">жетбаккупинстанце (JET_INSTANCE, String, баккупгрбит, JET_PFNSTATUS)</a> . Это самая простая и наиболее функциональная функция Restore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332995(v=exchg.10).md">Жетретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Ретриевеколумнгрбит, JET_RETINFO)</a></td>
<td>Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора. Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора. Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись. Помимо получения фактического значения столбца, Жетретриевеколумн можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn332997(v=exchg.10).md">Жетретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, Ретриевеколумнгрбит, JET_RETINFO)</a></td>
<td>Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора. Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора. Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись. Помимо получения фактического значения столбца, Жетретриевеколумн можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334004(v=exchg.10).md">жетретриевеколумнс</a></td>
<td>Получает несколько значений столбцов из текущей записи в одной операции. Массив структур JET_RETRIEVECOLUMN используется для описания набора значений столбцов для извлечения, а также для описания выходных буферов для каждого извлекаемого значения столбца.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334002(v=exchg.10).md">жетретриевекэй</a></td>
<td>Возвращает ключ для записи индекса в текущем положении курсора. См. также <a href="dn334085(v=exchg.10).md">ретриевекэй (JET_SESID, JET_TABLEID, ретриевекэйгрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334001(v=exchg.10).md">жетроллбакк</a></td>
<td>Отменяет изменения, внесенные в состояние базы данных, и возвращает его в последнюю точку сохранения. Жетроллбакк также закроет курсоры, открытые во время точки сохранения. Если внешняя точка сохранения отменена, сеанс завершит транзакцию.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334003(v=exchg.10).md">жетсик</a></td>
<td>Эффективно позиционирует курсор на запись индекса, которая соответствует условиям поиска, заданным в ключе поиска в этом курсоре, и заданному неравенству. Ключ поиска должен быть ранее создан с помощью <a href="dn292216(v=exchg.10).md">жетмакекэй (JET_SESID, JET_TABLEID, [], Int32, макекэйгрбит)</a>. См. также <a href="dn334145(v=exchg.10).md">трисик (JET_SESID, JET_TABLEID, сикгрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334009(v=exchg.10).md">Жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Сетколумнгрбит, JET_SETINFO)</a></td>
<td>Функция Жетсетколумн изменяет значение одного столбца в изменяемой записи, которое вставляется, или обновляет текущую запись. Он может перезаписать существующее значение, добавить новое значение в последовательность значений в столбце с несколькими значениями, удалить значение из последовательности значений в многозначном столбце или обновить все или часть длинного значения (столбец типа <a href="hh577895(v=exchg.10).md">LongText</a> или <a href="hh577895(v=exchg.10).md">лонгбинари</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334008(v=exchg.10).md">Жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Сетколумнгрбит, JET_SETINFO)</a></td>
<td>Функция Жетсетколумн изменяет значение одного столбца в изменяемой записи, которое вставляется, или обновляет текущую запись. Он может перезаписать существующее значение, добавить новое значение в последовательность значений в столбце с несколькими значениями, удалить значение из последовательности значений в многозначном столбце или обновить все или часть длинного значения (столбец типа <a href="hh577895(v=exchg.10).md">LongText</a> или <a href="hh577895(v=exchg.10).md">лонгбинари</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334010(v=exchg.10).md">жетсетколумндефаултвалуе</a></td>
<td>Изменяет значение существующего столбца по умолчанию.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334006(v=exchg.10).md">жетсетколумнс</a></td>
<td>Позволяет приложению задавать несколько значений столбцов в одной операции. Массив структур <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a> используется для описания набора значений столбцов, которые необходимо задать, а также для описания входных буферов для каждого устанавливаемого значения столбца.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334011(v=exchg.10).md">жетсеткуррентиндекс</a></td>
<td>Задает текущий индекс курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2</a></td>
<td>Задает текущий индекс курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3</a></td>
<td>Задает текущий индекс курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334013(v=exchg.10).md">JetSetCurrentIndex4</a></td>
<td>Задает текущий индекс курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334014(v=exchg.10).md">жетсетдатабасесизе</a></td>
<td>Задает размер неоткрытого файла базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334024(v=exchg.10).md">жетсетиндексранже</a></td>
<td>Временно ограничивает набор записей индекса, которые курсор может проанализировать с помощью <a href="dn292217(v=exchg.10).md">жетмове (JET_SESID, JET_TABLEID, Int32, мовегрбит)</a> , начиная с текущего элемента индекса и заканчивая записью индекса, которая соответствует критериям поиска, заданным в ключе поиска в этом курсоре, и указанным критериям привязки. Ключ поиска должен быть ранее создан с помощью <a href="dn292216(v=exchg.10).md">жетмакекэй (JET_SESID, JET_TABLEID, [], Int32, макекэйгрбит)</a>. См. также <a href="dn334099(v=exchg.10).md">трисетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334015(v=exchg.10).md">жетсетлс</a></td>
<td>позволяет приложению связать контекстный маркер, известный как локальный служба хранилища, с курсором или с таблицей, связанной с этим курсором. Этот обработчик контекста может использоваться приложением для хранения вспомогательных данных, связанных с курсором или таблицей. После этого приложение будет уведомлено с помощью обратного вызова времени выполнения, когда должен быть освобожден обработчик контекста. Это дает возможность связать динамически выделенное состояние с курсором или таблицей.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334027(v=exchg.10).md">жетсетсессионконтекст</a></td>
<td>Связывает сеанс с текущим потоком, используя заданный маркер контекста. Эта ассоциация переопределяет требование к подсистеме по умолчанию, что транзакция для данного сеанса должна полностью выполняться в том же потоке. Чтобы удалить связь, используйте <a href="dn332991(v=exchg.10).md">жетресетсессионконтекст (JET_SESID)</a> .</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334028(v=exchg.10).md">Жетсетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, строка)</a></td>
<td>Задает параметры конфигурации базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334017(v=exchg.10).md">Жетсетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, Int32, String)</a></td>
<td>Задает параметры конфигурации базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334029(v=exchg.10).md">Жетсетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</a></td>
<td>Задает параметры конфигурации базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334018(v=exchg.10).md">жетсеттаблесекуентиал</a></td>
<td>Уведомляет ядро СУБД о том, что приложение сканирует весь индекс, на котором расположен курсор. Следовательно, методы, используемые для доступа к данным индекса, будут настроены таким образом, чтобы сделать этот сценарий максимально быстрым. См. также <a href="dn332994(v=exchg.10).md">жетресеттаблесекуентиал (JET_SESID, JET_TABLEID, ресеттаблесекуентиалгрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334032(v=exchg.10).md">жетстопбаккупинстанце</a></td>
<td>Предотвращает продолжение операций потоковой архивации на определенном работающем экземпляре, тем самым завершая потоковую архивацию предсказуемым образом.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334035(v=exchg.10).md">жетстопсервицеинстанце</a></td>
<td>Подготавливает экземпляр к завершению.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334020(v=exchg.10).md">жеттерм</a></td>
<td>Завершите работу экземпляра, созданного с помощью <a href="dn292210(v=exchg.10).md">жетинит (JET_INSTANCE)</a> или <a href="dn292122(v=exchg.10).md">жеткреатеинстанце (JET_INSTANCE, String)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334037(v=exchg.10).md">JetTerm2</a></td>
<td>Завершите работу экземпляра, созданного с помощью <a href="dn292210(v=exchg.10).md">жетинит (JET_INSTANCE)</a> или <a href="dn292122(v=exchg.10).md">жеткреатеинстанце (JET_INSTANCE, String)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334022(v=exchg.10).md">жеттрункателогинстанце</a></td>
<td>Используется во время резервного копирования, инициированного Жетбегинекстерналбаккуп, для удаления всех файлов журнала транзакций, которые больше не понадобятся после успешного завершения текущего резервного копирования.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334019(v=exchg.10).md">жетунрегистеркаллбакк</a></td>
<td>Настраивает ядро СУБД на отмену отправки уведомлений приложению, которое было ранее запрошено через <a href="dn332989(v=exchg.10).md">жетрегистеркаллбакк (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334036(v=exchg.10).md">Жетупдате (JET_SESID, JET_TABLEID)</a></td>
<td>Функция Жетупдате выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки. Удаление строки таблицы выполняется путем вызова <a href="dn292131(v=exchg.10).md">жетделете (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334023(v=exchg.10).md">Жетупдате (JET_SESID, JET_TABLEID, [], Int32, Int32)</a></td>
<td>Функция Жетупдате выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки. Удаление строки таблицы выполняется путем вызова <a href="dn292131(v=exchg.10).md">жетделете (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334042(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, логическое значение, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334026(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, Byte, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334044(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, [], Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334025(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, DateTime, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334046(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, Double, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334030(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, GUID, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334048(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, Int16, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334031(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, Int32, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334050(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, Int64, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334033(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, Single, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334052(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, UInt16, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334054(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, UInt32, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334034(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, UInt64, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334038(v=exchg.10).md">Макекэй (JET_SESID, JET_TABLEID, строка, кодировка, Макекэйгрбит)</a></td>
<td>Конструирует ключ поиска, который затем может использоваться <a href="dn334003(v=exchg.10).md">жетсик (JET_SESID, JET_TABLEID, сикгрбит)</a> и <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334058(v=exchg.10).md">мовеафтерласт</a></td>
<td>Поместите курсор после последней записи в таблице. Последующее перемещение предыдущего положения курсора будет размещено на последней записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334057(v=exchg.10).md">мовебефорефирст</a></td>
<td>Установите курсор перед первой записью в таблице. Последующее перемещение будет размещать курсор на первой записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334040(v=exchg.10).md">ресетиндексранже</a></td>
<td>Удаляет диапазон индексов, созданный с помощью <a href="dn334024(v=exchg.10).md">жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a> или <a href="dn334099(v=exchg.10).md">трисетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)</a>. Если диапазон индекса отсутствует, этот метод не выполняет никаких действий.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит, JET_RETINFO)</a></td>
<td>Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора. Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора. Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись. Помимо получения фактического значения столбца, Жетретриевеколумн можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334045(v=exchg.10).md">Ретриевеколумнасбулеан (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение логического столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334078(v=exchg.10).md">Ретриевеколумнасбулеан (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение логического столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334047(v=exchg.10).md">Ретриевеколумнасбите (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение байтового столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334074(v=exchg.10).md">Ретриевеколумнасбите (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение байтового столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334077(v=exchg.10).md">Ретриевеколумнасдатетиме (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение столбца DateTime из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334051(v=exchg.10).md">Ретриевеколумнасдатетиме (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение столбца DateTime из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334053(v=exchg.10).md">Ретриевеколумнасдаубле (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение типа Double из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334084(v=exchg.10).md">Ретриевеколумнасдаубле (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение типа Double из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334056(v=exchg.10).md">Ретриевеколумнасфлоат (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение столбца с плавающей запятой из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334092(v=exchg.10).md">Ретриевеколумнасфлоат (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение столбца с плавающей запятой из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334093(v=exchg.10).md">Ретриевеколумнасгуид (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение столбца GUID из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334061(v=exchg.10).md">Ретриевеколумнасгуид (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение столбца GUID из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение столбца Int16 из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение столбца Int32 из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334067(v=exchg.10).md">Ретриевеколумнасстринг (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора. Используется кодировка Юникод.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334103(v=exchg.10).md">Ретриевеколумнасстринг (JET_SESID, JET_TABLEID, JET_COLUMNID, кодировка)</a></td>
<td>Извлекает значение строкового столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334070(v=exchg.10).md">Ретриевеколумнасстринг (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение строкового столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение столбца UInt16 из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение столбца UInt16 из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение столбца UInt32 из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение столбца UInt32 из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Извлекает значение столбца UInt64 из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</a></td>
<td>Извлекает значение столбца UInt64 из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334075(v=exchg.10).md">ретриевеколумнс</a></td>
<td>Извлекает столбцы в объекты Колумнвалуе.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334076(v=exchg.10).md">Ретриевеколумнсизе (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Получает размер значения одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора. Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора. Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334117(v=exchg.10).md">Ретриевеколумнсизе (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, Ретриевеколумнгрбит)</a></td>
<td>Получает размер значения одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора. Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора. Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334085(v=exchg.10).md">ретриевекэй</a></td>
<td>Возвращает ключ для записи индекса в текущем положении курсора.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334120(v=exchg.10).md">сериализеобжекттоколумн</a></td>
<td>Запись сериализованной формы объекта в столбец.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334123(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, логическое значение)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334080(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334121(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, [])</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334082(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334125(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334081(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, GUID)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334127(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334083(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334130(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334087(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, один)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334132(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334086(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334135(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334089(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Сетколумнгрбит)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334136(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, строка, кодировка)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334090(v=exchg.10).md">Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, строка, кодировка, Сетколумнгрбит)</a></td>
<td>Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334138(v=exchg.10).md">SetColumns</a></td>
<td>Задает столбцы из объектов Колумнвалуе.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334139(v=exchg.10).md">трижетлокк</a></td>
<td>Явно Зарезервируйте возможность обновления строки, блокировки записи или явного запрета обновления строки любым другим сеансом, блокировка чтения. Обычно блокировки записи строк получаются неявно в результате обновления строк. Блокировки чтения обычно не требуются из-за управления версиями записей. Однако в некоторых случаях транзакция может потребовать явно заблокировать строку для принудительного применения сериализации или убедиться, что дальнейшая операция будет выполнена.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334094(v=exchg.10).md">тримове</a></td>
<td>Попробуйте выполнить навигацию по индексу. Если переход выполнен, этот метод возвращает значение true. Если нет записи для перехода к этому методу, возвращает значение false; исключение будет создано для других ошибок.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334150(v=exchg.10).md">тримовефирст</a></td>
<td>Попробуйте перейти к первой записи в таблице. Если таблица пуста, возвращает значение false, если возникла другая ошибка, возникает исключение.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334140(v=exchg.10).md">тримовеласт</a></td>
<td>Попробуйте перейти к последней записи в таблице. Если таблица пуста, возвращает значение false, если возникла другая ошибка, возникает исключение.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334095(v=exchg.10).md">тримовенекст</a></td>
<td>Попробуйте перейти к следующей записи в таблице. Если следующая запись не возвращает значение false, то в случае возникновения другой ошибки возникает исключение.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334144(v=exchg.10).md">тримовепревиаус</a></td>
<td>Попробуйте перейти к предыдущей записи в таблице. Если Предыдущая запись отсутствует, возвращает значение false, если возникла другая ошибка, возникает исключение.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334096(v=exchg.10).md">трйопентабле</a></td>
<td>Попробуйте открыть таблицу.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334145(v=exchg.10).md">трисик</a></td>
<td>Эффективно позиционирует курсор на запись индекса, которая соответствует условиям поиска, заданным в ключе поиска в этом курсоре, и заданному неравенству. Ключ поиска должен быть ранее создан с помощью Жетмакекэй.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn334099(v=exchg.10).md">трисетиндексранже</a></td>
<td>Временно ограничивает набор записей индекса, которые курсор может проанализировать с помощью Жетмове, начиная с текущего элемента индекса и заканчивая элементом индекса, который соответствует критериям поиска, заданным в этом курсоре, и указанным критериям. Ключ поиска должен быть ранее создан с помощью Жетмакекэй. Возвращает значение true, если диапазон индекса не является пустым, и false в противном случае.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
