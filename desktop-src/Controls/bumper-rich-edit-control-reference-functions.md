---
title: Функции расширенного редактирования
description: Функции расширенного редактирования
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1b74069b63220a07bfb1bd5e3f5a1ad99a6c6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482460"
---
# <a name="rich-edit-functions"></a>Функции расширенного редактирования

## <a name="in-this-section"></a>В этом разделе




| Раздел | Описание | 
|-------|-------------|
| <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>аутокорректпрок</em></a><br /> | Функция <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>аутокорректпрок</em></a> является определяемой приложением функцией обратного вызова, которая используется с сообщением <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .<br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>едитстреамкаллбакк</em></a><br /> | Функция <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>едитстреамкаллбакк</em></a> — это определяемая приложением функция обратного вызова, используемая с сообщениями <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> и <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> . Он используется для передачи потока данных в элемент управления Rich Edit или из него. Тип <strong>едитстреамкаллбакк</strong> определяет указатель на эту функцию обратного вызова. <em>Едитстреамкаллбакк</em> — это заполнитель для имени определяемой приложением функции. <br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>едитвордбреакпроцекс</em></a><br /> | Функция <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>едитвордбреакпроцекс</em></a> — это определяемая приложением функция обратного вызова, используемая с сообщением <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> . Он определяет индекс символа разрыва слова или класс символов и флаги разрыва слова для символов в указанном тексте. Тип <strong>едитвордбреакпроцекс</strong> определяет указатель на эту функцию обратного вызова. <em>Едитвордбреакпроцекс</em> — это заполнитель для имени определяемой приложением функции. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>жетмасалфанумерик</strong></a><br /> | Извлекает формат преобразования Юникода (UTF) — 32 математический алфавитный символ, соответствующий заданному базовому символу многоязыковой плоскости (BMP) и стилю математических символов. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>жетмасалфанумериккоде</strong></a><br /> | Извлекает стиль математических символов и базовый код, соответствующий заданному замыкающему байту пары математических знаков.<br /> | 
| <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>хифенатепрок</em></a><br /> | Функция <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>хифенатепрок</em></a> — это определяемая приложением функция обратного вызова, используемая с сообщением <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> . Он определяет, как расстановка переносов выполняется в элементе управления Microsoft Rich Edit.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>масбуилддовн</strong></a><br /> | Преобразует встроенный математический, Ruby и другие встроенные объекты в указанном диапазоне в линейную форму.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>масбуилдуп</strong></a><br /> | Преобразует математические значения линейного формата в диапазоне в встроенную форму или изменяет текущую встроенную форму. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>мастранслате</strong></a><br /> | Преобразует математические символы в указанном диапазоне.<br /> | 
| <a href="reextendedregisterclass.md"><strong>рикстендедрегистеркласс</strong></a><br /> | Регистрирует два имени класса, REListBox20W и RECombobox20W, которые можно использовать для создания окон с широкими возможностями редактирования или ComboBox. <br /><blockquote>[!Note]<br />Предназначен для внутреннего использования; не рекомендуется для использования в приложениях. Эта функция может не поддерживаться в будущих версиях.</blockquote><br /> | 




 

 

