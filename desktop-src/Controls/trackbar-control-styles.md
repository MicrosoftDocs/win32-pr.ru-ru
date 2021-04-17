---
title: Стили элементов управления TrackBar (Коммктрл. h)
description: В этом разделе содержатся сведения о стилях, используемых для элементов управления TrackBar.
ms.assetid: ac2f59c6-85a2-4f41-aace-4132971d3559
topic_type:
- apiref
api_name:
- TBS_AUTOTICKS
- TBS_VERT
- TBS_HORZ
- TBS_TOP
- TBS_BOTTOM
- TBS_LEFT
- TBS_RIGHT
- TBS_BOTH
- TBS_NOTICKS
- TBS_ENABLESELRANGE
- TBS_FIXEDLENGTH
- TBS_NOTHUMB
- TBS_TOOLTIPS
- TBS_REVERSED
- TBS_DOWNISLEFT
- TBS_NOTIFYBEFOREMOVE
- TBS_TRANSPARENTBKGND
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42966f98db18257c9a6a9ca463d5bd88028a02f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657150"
---
# <a name="trackbar-control-styles"></a>Стили элемента управления TrackBar

В этом разделе содержатся сведения о стилях, используемых для элементов управления TrackBar.



| Константа                                                                                                                                                                           | Описание                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**\_АВТОтакты TBS**</dt> </dl>                      | Элемент управления TrackBar имеет деление на каждое приращение в диапазоне значений. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**TBS по \_ вертикали**</dt> </dl>                                     | Элемент управления TrackBar ориентирован вертикально.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**TBS \_ горизонтали**</dt> </dl>                                     | Элемент управления TrackBar ориентирован горизонтально. Это ориентация по умолчанию. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**\_Начало TBS**</dt> </dl>                                        | Элемент управления TrackBar отображает деления над элементом управления. Этот стиль действителен только с TBS \_ горизонтали. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**\_конец TBS**</dt> </dl>                               | Элемент управления TrackBar отображает деления под элементом управления. Этот стиль действителен только с TBS \_ горизонтали. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**\_Left TBS**</dt> </dl>                                     | Элемент управления TrackBar отображает деления слева от элемента управления. Этот стиль допустим только для TBS по \_ вертикали. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**право на TBS \_**</dt> </dl>                                  | Элемент управления TrackBar отображает деления справа от элемента управления. Этот стиль допустим только для TBS по \_ вертикали. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TBS \_**</dt> </dl>                                     | Элемент управления TrackBar отображает деления на обеих сторонах элемента управления. Они будут как сверху, так и снизу при использовании с TBS \_ горизонтали или обоими слева и справа при использовании с TBS по \_ вертикали. <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**\_апострофы TBS**</dt> </dl>                            | Элемент управления TrackBar не отображает деления. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**TBS \_ енаблеселранже**</dt> </dl>       | Элемент управления TrackBar отображает только диапазон выбора. Деления на начальном и конечном позиции диапазона выбора отображаются в виде треугольников (вместо вертикальных штрихов), а выделенный диапазон выделяется. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**TBS \_ FIXEDLENGTH**</dt> </dl>                | Элемент управления TrackBar позволяет изменить размер ползунка с помощью сообщения [**ТБМ \_ сетсумбленгс**](tbm-setthumblength.md) . <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**\_ПОДбегунок TBS**</dt> </dl>                            | Элемент управления TrackBar не отображает ползунок. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**\_подсказки TBS**</dt> </dl>                         | [Версия 4,70](common-control-versions.md). Элемент управления TrackBar поддерживает подсказки. При создании элемента управления TrackBar с помощью этого стиля автоматически создается элемент управления ToolTip по умолчанию, который отображает текущую положение ползунка. Вы можете изменить место отображения всплывающих подсказок с помощью сообщения [**ТБМ \_ сеттипсиде**](tbm-settipside.md) . <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**обращение в TBS \_**</dt> </dl>                         | [Версия 5,80.](common-control-versions.md) Этот бит стиля используется для "обратных" значений TrackBar, где меньшее число означает "выше", а большее — "ниже". Он не влияет на элемент управления; Это просто метка, которую можно проверить, чтобы определить, является ли значение TrackBar нормальным или обратным.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**TBS \_ довнислефт**</dt> </dl>                   | По умолчанию элемент управления TrackBar использует значение вниз, равное правому и левому. Используйте стиль TBS \_ довнислефт для отмены значения по умолчанию, сделав его нажатым слева и вверх равным право. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**TBS \_ нотифибефоремове**</dt> </dl> | [Версии 6,00](common-control-versions.md) и **Windows Vista.** Значение TrackBar должно уведомлять родительский элемент перед изменением положения ползунка из-за действия пользователя (включает привязку). <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**TBS \_ транспарентбкгнд**</dt> </dl> | [Версии 6,00](common-control-versions.md) и **Windows Vista.** Фон закрашивается родительским объектом через \_ сообщение WM принтклиент. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





