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
ms.openlocfilehash: aff6116433533bdc79535be0e282cb81baa9368f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470626"
---
# <a name="animation-control-styles"></a>Стили элементов управления анимацией

В этом разделе перечислены стили окон, используемые с элементами управления "анимация".




| Константа | Описание | 
|----------|-------------|
| <span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl><dt><strong>ACS_AUTOPLAY</strong></dt></dl> | Запускает воспроизведение анимации сразу после открытия AVI-файла. <br /> | 
| <span id="ACS_CENTER"></span><span id="acs_center"></span><dl><dt><strong>ACS_CENTER</strong></dt></dl> | Центрирование анимации в окне анимированного элемента управления. <br /> | 
| <span id="ACS_TIMER"></span><span id="acs_timer"></span><dl><dt><strong>ACS_TIMER</strong></dt></dl> | По умолчанию элемент управления создает поток для воспроизведения фрагмента AVI. Если установить этот флаг, элемент управления воспроизводит клип, не создавая поток; на внутреннем уровне элемент управления использует таймер Win32 для синхронизации воспроизведения. <br /><strong>Comctl32.dll версии 6 и более поздних версий:</strong> Этот стиль не поддерживается. По умолчанию элемент управления воспроизводит ролик AVI без создания потока.<br /><blockquote>[!Note]<br />Версия Comctl32.dll 6 не является распространяемой. Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте. Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.</blockquote><br /> | 
| <span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl><dt><strong>ACS_TRANSPARENT</strong></dt></dl> | Позволяет сопоставить цвет фона анимации с основным окном, создавая "прозрачный" фон. У родителя элемента управления анимации не должно быть стиля WS_CLIPCHILDREN (см. раздел <a href="/windows/desktop/winmsg/window-styles">стили окна</a>). Элемент управления отправляет <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> сообщение родительскому объекту. Используйте <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>сетбкколор</strong></a> , чтобы задать в качестве цвета фона для контекста устройства соответствующее значение. Элемент управления интерпретирует верхний левый пиксел первого кадра как цвет фона анимации по умолчанию. Он выполнит сопоставление всех пикселей с этим цветом и значением, которое вы указали в ответе на WM_CTLCOLORSTATIC. <br /> | 




## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



