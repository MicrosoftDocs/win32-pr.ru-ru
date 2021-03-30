---
title: Вызов WDS из командной строки
description: Вы можете запустить пользовательский интерфейс Microsoft Windows Desktop Search (WDS) с конкретным фильтром, хранилищем и запросом из другого приложения или веб-страницы, использующей объект модуля поддержки браузера (BHO), с помощью синтаксиса командной строки windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "103789162"
---
# <a name="calling-wds-from-the-command-line"></a>Вызов WDS из командной строки

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .

Вы можете запустить пользовательский интерфейс Microsoft Windows Desktop Search (WDS) с конкретным фильтром, хранилищем и запросом из другого приложения или веб-страницы, использующей объект модуля поддержки браузера (BHO), с помощью синтаксиса командной строки windowssearch.exe. При вызове WDS из командной строки сведения о действиях пользователя или выборе в окне WDS не возвращаются вызывающему приложению или веб-странице.

Путь установки WDS указывается в параметре реестра InstallDir в разделе HKEY_LOCAL_MACHINE \\ Software \\ Microsoft \\ Windows Desktop Search. Путь по умолчанию, по которому устанавливается windowssearch.exe, — это Program Files \\ Windows Desktop Search.

## <a name="command-line-syntax"></a>Синтаксис командной строки

Следующий синтаксис применяется к интерфейсу командной строки Windows Desktop Search 2. x.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Параметры</th>
<th>Параметр</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/стартуп</td>

<td>Инициализирует панель поиска Windows</td>
</tr>
<tr class="even">
<td>/индекснов</td>

<td>Отключает отключать индексацию и повторно сканирует все расположения индексов</td>
</tr>
<tr class="odd">
<td>/шовстатус</td>

<td>Отображение окна состояния индексирования</td>
</tr>
<tr class="even">
<td>/лаунчсеарчвиндов или/УРЛ</td>

<td>Открывает окно WDS с пустым запросом</td>
</tr>
<tr class="odd">
<td>/урл</td>
<td>Поиск: [магазин | отображение | запрос] строка запроса</td>
<td>Открывает окно WDS с запросом и фильтром на основе следующих параметров:
<ul>
<li><p>хранилище — указывает источник данных для запроса: файлы, Outlook, аутлукекспресс. Если не указано, будет выполнен поиск по всем хранилищам. <br/></p>
<blockquote>
[!Note]<br />
Хотя расширенный синтаксис запросов поддерживает ссылку на Microsoft Outlook как OE, параметр Store в командной строке должен иметь значение "аутлукекспресс".
</blockquote>
<p><br/></p></li>
<li><p>показывать — указывает наблюдаемый тип возвращаемых результатов. Полный список типов см. в разделе <a href="-search-2x-wds-perceivedtype.md">наблюдаемые типы</a> . Если не указано, будут возвращены все типы. <br/></p>
<blockquote>
[!Note]<br />
Существует три различия между значениями воспринимаемого типа и значениями для представления. Для <code>show</code> Используйте "Documents" вместо "doc", "Pictures" вместо "pics" и "текстдокументс" вместо "Text".
</blockquote>
<p><br/></p></li>
<li>запрос — задает условие поиска. Это значение поддерживает <a href="-search-2x-wds-aqsreference.md">Расширенные параметры синтаксиса запросов</a> для уточнения результатов. Параметр запроса должен быть последним параметром в URL-адресе.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>Пример

Например, для поиска изображений по всем файлам, соответствующим критерию "фоновый рисунок", используйте следующую команду:

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Синтаксис расширенных запросов](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Наблюдаемые типы](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Вызов WDS из веб-страниц](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





