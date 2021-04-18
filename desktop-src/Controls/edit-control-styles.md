---
title: Стили элемента управления Edit (Winuser. h)
description: Чтобы создать элемент управления "поле ввода" с помощью функции CreateWindow или CreateWindowEx, укажите класс EDIT, соответствующие константы стиля окна и сочетание следующих стилей элемента управления Edit.
ms.assetid: 336c69b7-bc23-4b93-8968-ad63a1703385
topic_type:
- apiref
api_name:
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_LOWERCASE
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_OEMCONVERT
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_UPPERCASE
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 9b255aee665c32f9a14be4946dee0122dad626bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648635"
---
# <a name="edit-control-styles"></a>Изменить стили элемента управления

Чтобы создать элемент управления "поле ввода" с помощью функции [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , укажите класс Edit, соответствующие константы стиля окна и сочетание следующих стилей элемента управления Edit. После создания элемента управления эти стили нельзя изменить, за исключением указанных.

## <a name="example"></a>Пример

```cpp
LRESULT MsgCreate(HWND hwnd, UINT uMessage, WPARAM wparam, LPARAM lparam)
{
    lparam;
    wparam;
    uMessage;

    // Create Edit control for typing to be sent to server
    if (NULL == (hOutWnd = CreateWindow("EDIT",
                           NULL,
                           WS_BORDER | WS_CHILD | WS_VISIBLE | WS_VSCROLL | ES_LEFT | 
                           ES_MULTILINE | ES_AUTOVSCROLL,
                           0,0,0,0,
                           hwnd,
                           (HMENU) ID_OUTBOX,
                           (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE),
                           NULL)))
        return FALSE;
    return TRUE;
}
```

Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) на сайте GitHub.

## <a name="constants"></a>Константы

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt><strong>ES_AUTOHSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Автоматически прокручивает текст вправо на 10 символов, когда пользователь вводит символ в конце строки. Когда пользователь нажимает клавишу ВВОД, элемент управления прокручивает весь текст обратно в нулевое расположение.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt><strong>ES_AUTOVSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Автоматически прокручивает текст вверх на одну страницу, когда пользователь нажимает клавишу ВВОД в последней строке.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt><strong>ES_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Центрирование текста в однострочном или многострочном элементе управления Edit.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt><strong>ES_LEFT</strong></dt> </dl></td>
<td style="text-align: left;">Выровняйте текст по левому полю.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <dt><strong>ES_LOWERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Преобразует все символы в нижний регистр по мере их ввода в элемент управления "поле ввода".<br/> Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt><strong>ES_MULTILINE</strong></dt> </dl></td>
<td style="text-align: left;">Задает многострочный элемент управления Edit. Значение по умолчанию — однострочный элемент управления Edit. <br/> Если элемент управления "поле ввода" находится в диалоговом окне, то по умолчанию нажатием клавиши Ввод выполняется активация кнопки по умолчанию. Чтобы использовать клавишу ВВОД в качестве возврата каретки, используйте стиль <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .<br/> Если элемент управления "поле ввода" не находится в диалоговом окне и указан стиль <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> , элемент управления "поле ввода" отображает как можно больше строк и прокручивает по вертикали, когда пользователь нажимает клавишу ВВОД. Если не указать <strong>ES_AUTOVSCROLL</strong>, в элементе управления "поле ввода" отображается столько строк, сколько возможно, и звуковые сигналы, если пользователь нажмет клавишу ВВОД, когда больше не удастся отобразить какие бы то ни было строки.<br/> Если указать стиль <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , то многострочный элемент управления "поле ввода" автоматически прокручивается горизонтально, когда курсор выходит за правый края элемента управления. Чтобы начать новую строку, пользователь должен нажать клавишу ВВОД. Если не указать <strong>ES_AUTOHSCROLL</strong>, элемент управления автоматически заключает слова в начало следующей строки, если это необходимо. Новая строка также запускается, если пользователь нажмет клавишу ВВОД. Размер окна определяет расположение переданного слова. Если размер окна изменяется, то в Вордвраппинг положении изменяется и текст отображается повторно.<br/> Элементы управления для многострочного редактирования могут иметь полосы прокрутки. Элемент управления "Правка" с полосами прокрутки обрабатывает собственные сообщения с полосой прокрутки. Обратите внимание, что элементы управления редактирования без полос прокрутки прокручиваться, как описано в предыдущих абзацах, и обрабатывают все сообщения, отправленные родительским окном.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt><strong>ES_NOHIDESEL</strong></dt> </dl></td>
<td style="text-align: left;">Инвертирует поведение по умолчанию для элемента управления "поле ввода". Поведение по умолчанию скрывает выделение, когда элемент управления теряет фокус ввода и инвертирует выбор, когда элемент управления получает фокус ввода. Если указать <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, выделенный текст будет инвертирован, даже если элемент управления не имеет фокуса.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt><strong>ES_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Позволяет указывать в элементе управления "поле ввода" только цифры. Обратите внимание, что даже при использовании этого набора все равно можно вставить нецифры в элемент управления Edit. <br/> Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/> Чтобы перевести текст, который был вставлен в элемент управления "поле ввода", в целочисленное значение, используйте функцию <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>жетдлгитеминт</strong></a> . Чтобы задать для текста элемента управления "поле ввода" строковое представление указанного целого числа, используйте функцию <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>сетдлгитеминт</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <dt><strong>ES_OEMCONVERT</strong></dt> </dl></td>
<td style="text-align: left;">Преобразует текст, указанный в элементе управления "поле ввода". Текст преобразуется из набора символов Windows в набор символов OEM, а затем обратно в набор символов Windows. Это обеспечивает правильное преобразование символов, когда приложение вызывает функцию <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>чартуем</strong></a> для преобразования строки Windows в элементе управления "поле ввода" в символы OEM. Этот стиль наиболее удобен для элементов управления для редактирования, содержащих имена файлов, которые будут использоваться в файловых системах, не поддерживающих Юникод. <br/> Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt><strong>ES_PASSWORD</strong></dt> </dl></td>
<td style="text-align: left;">Отображает звездочку (*) для каждого символа, вводимого в элемент управления "поле ввода". Этот стиль допустим только для однострочных элементов управления редактирования. <br/> Чтобы изменить отображаемые символы или установить или снять этот стиль, используйте <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> сообщение. <br/>
<blockquote>
[!Note]<br />
Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте. Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt><strong>ES_READONLY</strong></dt> </dl></td>
<td style="text-align: left;">Не разрешает пользователю вводить или редактировать текст в элементе управления "поле ввода".<br/> Чтобы изменить стиль после создания элемента управления, используйте <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> сообщение. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt><strong>ES_RIGHT</strong></dt> </dl></td>
<td style="text-align: left;">Выровнять текст по правому краю в однострочном или многострочном элементе управления Edit.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <dt><strong>ES_UPPERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Преобразует все символы в верхний регистр по мере их ввода в элемент управления "поле ввода". <br/> Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt><strong>ES_WANTRETURN</strong></dt> </dl></td>
<td style="text-align: left;">Указывает, что возврат каретки должен быть вставлен, когда пользователь нажимает клавишу ВВОД при вводе текста в многострочный элемент управления "поле ввода" в диалоговом окне. Если этот стиль не указан, нажатие клавиши ВВОД приведет к тому же результату, что и нажатие кнопки по умолчанию в диалоговом окне. Этот стиль не влияет на однострочный элемент управления Edit. <br/> Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h</dt> </dl> |



