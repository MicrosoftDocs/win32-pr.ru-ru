---
title: Стили элементов управления анимацией (Коммктрл. h)
description: В этом разделе перечислены стили окон, используемые с элементами управления "анимация".
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657261"
---
# <a name="animation-control-styles"></a>Стили элементов управления анимацией

В этом разделе перечислены стили окон, используемые с элементами управления "анимация".



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
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <dt><strong>ACS_AUTOPLAY</strong></dt> </dl></td>
<td style="text-align: left;">Запускает воспроизведение анимации сразу после открытия AVI-файла. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <dt><strong>ACS_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Центрирование анимации в окне анимированного элемента управления. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <dt><strong>ACS_TIMER</strong></dt> </dl></td>
<td style="text-align: left;">По умолчанию элемент управления создает поток для воспроизведения фрагмента AVI. Если установить этот флаг, элемент управления воспроизводит клип, не создавая поток; на внутреннем уровне элемент управления использует таймер Win32 для синхронизации воспроизведения. <br/> <strong>Comctl32.dll версии 6 и более поздних версий:</strong> Этот стиль не поддерживается. По умолчанию элемент управления воспроизводит ролик AVI без создания потока.<br/>
<blockquote>
[!Note]<br />
Версия Comctl32.dll 6 не является распространяемой. Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте. Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <dt><strong>ACS_TRANSPARENT</strong></dt> </dl></td>
<td style="text-align: left;">Позволяет сопоставить цвет фона анимации с основным окном, создавая &quot; прозрачный &quot; фон. У родителя элемента управления анимации не должно быть стиля WS_CLIPCHILDREN (см. раздел <a href="/windows/desktop/winmsg/window-styles">стили окна</a>). Элемент управления отправляет <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> сообщение родительскому объекту. Используйте <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>сетбкколор</strong></a> , чтобы задать в качестве цвета фона для контекста устройства соответствующее значение. Элемент управления интерпретирует верхний левый пиксел первого кадра как цвет фона анимации по умолчанию. Он выполнит сопоставление всех пикселей с этим цветом и значением, которое вы указали в ответе на WM_CTLCOLORSTATIC. <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



