---
title: Функции расширенного редактирования
description: Функции расширенного редактирования
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105651478"
---
# <a name="rich-edit-functions"></a>Функции расширенного редактирования

## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>аутокорректпрок</em></a><br/></td>
<td>Функция <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>аутокорректпрок</em></a> является определяемой приложением функцией обратного вызова, которая используется с сообщением <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>едитстреамкаллбакк</em></a><br/></td>
<td>Функция <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>едитстреамкаллбакк</em></a> — это определяемая приложением функция обратного вызова, используемая с сообщениями <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> и <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> . Он используется для передачи потока данных в элемент управления Rich Edit или из него. Тип <strong>едитстреамкаллбакк</strong> определяет указатель на эту функцию обратного вызова. <em>Едитстреамкаллбакк</em> — это заполнитель для имени определяемой приложением функции. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>едитвордбреакпроцекс</em></a><br/></td>
<td>Функция <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>едитвордбреакпроцекс</em></a> — это определяемая приложением функция обратного вызова, используемая с сообщением <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> . Он определяет индекс символа разрыва слова или класс символов и флаги разрыва слова для символов в указанном тексте. Тип <strong>едитвордбреакпроцекс</strong> определяет указатель на эту функцию обратного вызова. <em>Едитвордбреакпроцекс</em> — это заполнитель для имени определяемой приложением функции. <br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>жетмасалфанумерик</strong></a><br/></td>
<td>Извлекает формат преобразования Юникода (UTF) — 32 математический алфавитный символ, соответствующий заданному базовому символу многоязыковой плоскости (BMP) и стилю математических символов. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>жетмасалфанумериккоде</strong></a><br/></td>
<td>Извлекает стиль математических символов и базовый код, соответствующий заданному замыкающему байту пары математических знаков.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>хифенатепрок</em></a><br/></td>
<td>Функция <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>хифенатепрок</em></a> — это определяемая приложением функция обратного вызова, используемая с сообщением <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> . Он определяет, как расстановка переносов выполняется в элементе управления Microsoft Rich Edit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>масбуилддовн</strong></a><br/></td>
<td>Преобразует встроенный математический, Ruby и другие встроенные объекты в указанном диапазоне в линейную форму.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>масбуилдуп</strong></a><br/></td>
<td>Преобразует математические значения линейного формата в диапазоне в встроенную форму или изменяет текущую встроенную форму. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>мастранслате</strong></a><br/></td>
<td>Преобразует математические символы в указанном диапазоне.<br/></td>
</tr>
<tr class="even">
<td><a href="reextendedregisterclass.md"><strong>рикстендедрегистеркласс</strong></a><br/></td>
<td>Регистрирует два имени класса, REListBox20W и RECombobox20W, которые можно использовать для создания окон с широкими возможностями редактирования или ComboBox. <br/>
<blockquote>
[!Note]<br />
Предназначен для внутреннего использования; не рекомендуется для использования в приложениях. Эта функция может не поддерживаться в будущих версиях.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

