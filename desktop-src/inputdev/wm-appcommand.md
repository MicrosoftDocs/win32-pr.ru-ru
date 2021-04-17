---
title: Сообщение WM_APPCOMMAND (Winuser. h)
description: Уведомляет окно о том, что пользователь создал событие команды приложения, например, щелкнув кнопку команды приложения с помощью мыши или введя клавишу команды приложения на клавиатуре.
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- WM_APPCOMMAND ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_APPCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7f5e71f9a443e12ea56cb8ca23daea148da92aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415305"
---
# <a name="wm_appcommand-message"></a>\_Сообщение АППКОММАНД WM

Уведомляет окно о том, что пользователь создал событие команды приложения, например, щелкнув кнопку команды приложения с помощью мыши или введя клавишу команды приложения на клавиатуре.


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер окна, в котором пользователь нажимает кнопку или нажал клавишу. Это может быть дочернее окно окна, получающего сообщение. Дополнительные сведения об обработке этого сообщения см. в разделе "Примечания".

</dd> <dt>

*lParam* 
</dt> <dd>

Используйте следующий код, чтобы получить сведения, содержащиеся в параметре *lParam* .


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



Команда приложения — *cmd*, которая может принимать одно из следующих значений.



| Значение                                                                                                                                                                                                                                                                                                                  | Значение                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**Аппкомманд \_ \_Увеличение басов**</dt> <dt>20</dt> </dl>                                                                         | Включение и отключение увеличения басов.<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**Аппкомманд \_ БАСОВ \_ вниз**</dt> <dt>19</dt> </dl>                                                                            | Уменьшите низкие частоты.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**Аппкомманд \_ Низкие \_ частоты**</dt> на <dt>21</dt> </dl>                                                                                  | Увеличьте низкие частоты.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**Аппкомманд \_ БРАУЗЕР \_ назад**</dt> <dt>1</dt> </dl>                                                        | Перейдите назад.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**Аппкомманд \_ \_Избранное браузера**</dt> <dt>6</dt> </dl>                                                     | Откройте Избранное.<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**Аппкомманд \_ БРАУЗЕР \_ вперед**</dt> <dt>2</dt> </dl>                                                           | Перейдите вперед.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**Аппкомманд \_ Обозреватель \_ Home**</dt> <dt>7</dt> </dl>                                                                    | Перейдите домой.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**Аппкомманд \_ \_Обновление обозревателя**</dt> <dt>3</dt> </dl>                                                           | Обновить страницу.<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**Аппкомманд \_ \_Поиск в браузере**</dt> <dt>5</dt> </dl>                                                              | Откройте Поиск.<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**Аппкомманд \_ БРАУЗЕР \_ останавливается**</dt> <dt>4</dt> </dl>                                                                    | Останавливает скачивание.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**Аппкомманд \_ ЗАКРЫТЬ**</dt> <dt>31</dt> </dl>                                                                                         | Закройте окно (не приложение).<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**Аппкомманд \_ КОПИРОВАНИЕ**</dt> <dt>36</dt> </dl>                                                                                            | Скопируйте выделенный фрагмент.<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**Аппкомманд \_ \_Список исправлений**</dt> <dt>45</dt> </dl>                                                          | Отображает список исправлений, если слово неправильно идентифицируется во время речевого ввода. <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**Аппкомманд \_ Вырезание**</dt> <dt>37</dt> </dl>                                                                                               | Вырезать выделенный фрагмент.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**Аппкомманд \_ Режим ДИКТОВКи \_ или \_ управления командами \_ \_ Переключить**</dt> <dt>43</dt> </dl> | Переключение между двумя режимами речевого ввода: Диктовка и команда/управление (предоставление команд приложению или доступ к меню). <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**Аппкомманд \_ НАЙТИ**</dt> <dt>28</dt> </dl>                                                                                            | Откройте диалоговое окно **найти** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**Аппкомманд \_ Пересылка \_ почты**</dt> <dt>40</dt> </dl>                                                                   | Пересылка почтового сообщения.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**Аппкомманд \_ Справка**</dt> <dt>27</dt> </dl>                                                                                            | Откройте диалоговое окно **справки** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**Аппкомманд \_ ЗАПУСК \_ APP1**</dt> <dt>17</dt> </dl>                                                                      | Запустите App1.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**Аппкомманд \_ ЗАПУСК \_**</dt> до <dt>18 лет</dt> </dl>                                                                      | Запустите.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**Аппкомманд \_ ЗАПУСК \_ сообщения**</dt> <dt>15</dt> </dl>                                                                      | Откройте почту.<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**Аппкомманд \_ ЗАПУСК \_ носителя \_ SELECT**</dt> <dt>16</dt> </dl>                                             | Перейдите в режим выбор носителя.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**Аппкомманд \_ \_Канал мультимедиа \_**</dt> , <dt>52</dt> </dl>                                                | Уменьшите значение канала, например, для телевизора или радио-тюнера. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**Аппкомманд \_ \_Канал мультимедиа \_ up**</dt> <dt>51</dt> </dl>                                                      | Увеличьте значение канала, например, для телевизора или радио-тюнера. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**Аппкомманд \_ МЕДИА \_ fast \_ вперед**</dt> <dt>49</dt> </dl>                                                | Увеличение скорости воспроизведения потока. Это можно реализовать множеством способов, например с помощью фиксированной скорости или переключения по ряду возрастающей скорости. <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**Аппкомманд \_ MEDIA \_ нексттракк**</dt> <dt>11</dt> </dl>                                                          | Перейдите к следующей дорожке.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**Аппкомманд \_ MEDIA \_ PAUSE**</dt> <dt>47</dt> </dl>                                                                      | Приостановка. Если работа уже приостановлена, дальнейших действий не требуется. Это команда прямой приостановки, которая не имеет состояния. Если существуют дискретные кнопки воспроизведения и паузы, приложения должны предпринять действия с этой командой, а также **аппкомманд \_ Media \_ Play \_ Pause**. <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**Аппкомманд \_ MEDIA \_ PLAY**</dt> <dt>46</dt> </dl>                                                                         | Начало воспроизведения в текущей позиции. Если она уже приостановлена, она возобновится. Это команда прямого воспроизведения, которая не имеет состояния. Если существуют дискретные кнопки **воспроизведения** и **паузы** , приложения должны предпринять действия с этой командой, а также **аппкомманд \_ Media \_ Play \_ Pause**.<br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**Аппкомманд \_ \_Воспроизведение мультимедиа \_ приостановлено**</dt> <dt>14</dt> </dl>                                                      | Воспроизведение или приостановка воспроизведения. Если существуют дискретные кнопки **воспроизведения** и **паузы** , приложения должны предпринять действия с этой командой, а также **аппкомманд \_ Media \_ Play** и **аппкомманд \_ Media \_ Pause**.<br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**Аппкомманд \_ MEDIA \_ превиаустракк**</dt> <dt>12</dt> </dl>                                              | Переход к предыдущей дорожке.<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**Аппкомманд \_ \_Запись носителя**</dt> <dt>48</dt> </dl>                                                                   | Начать запись текущего потока.<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**Аппкомманд \_ \_Перемотка носителей**</dt> <dt>50</dt> </dl>                                                                   | Перейдем назад в потоке с более высокой скоростью. Это можно реализовать множеством способов, например с помощью фиксированной скорости или переключения по ряду возрастающей скорости. <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**Аппкомманд \_ MEDIA \_ останавливает**</dt> <dt>13</dt> </dl>                                                                         | Останавливает воспроизведение.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**Аппкомманд \_ Вкл. вкл. 44 \_ \_ \_ /выкл**</dt> . <dt></dt> </dl>                                                  | Переключить микрофон.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**Аппкомманд \_ \_Громкость \_ микрофона**</dt> , <dt>25</dt> </dl>                                    | Уменьшение громкости микрофона.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**Аппкомманд \_ \_ \_ Выкл. громкость микрофона**</dt> <dt>24</dt> </dl>                                    | Отключите микрофон.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**Аппкомманд \_ \_Громкость \_ микрофона**</dt> , <dt>26</dt> </dl>                                          | Увеличение громкости микрофона.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**Аппкомманд \_ НОВЫЕ**</dt> <dt>29</dt> </dl>                                                                                               | Создание нового окна.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**Аппкомманд \_ ОТКРЫТО**</dt> <dt>30</dt> </dl>                                                                                            | Откройте окно.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**Аппкомманд \_ Вставьте**</dt> <dt>38</dt> </dl>                                                                                         | Вставить<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**Аппкомманд \_ Печать**</dt> <dt>33</dt> </dl>                                                                                         | Печать текущего документа.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**Аппкомманд \_ Повтор**</dt> <dt>35</dt> </dl>                                                                                            | Повторить последнее действие.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**Аппкомманд \_ ОТВЕТ \_ на \_ электронную почту**</dt> <dt>39</dt> </dl>                                                               | Ответ на почтовое сообщение.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**Аппкомманд \_ СОХРАНЕНИЕ**</dt> <dt>32</dt> </dl>                                                                                            | Сохранить текущий документ.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**Аппкомманд \_ Отправка \_ почты**</dt> <dt>41</dt> </dl>                                                                            | Отправка почтового сообщения.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**Аппкомманд \_ \_Проверка орфографии**</dt> <dt>42</dt> </dl>                                                                      | Запустите проверку орфографии.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**Аппкомманд \_ \_Со высоких частотой**</dt> <dt>22</dt> </dl>                                                                      | Уменьшение высоких частот.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**Аппкомманд \_ Высокие частоты \_**</dt> <dt>23</dt> </dl>                                                                            | Увеличьте уровень высоких частот.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**Аппкомманд \_ UNDO**</dt> <dt>34</dt> </dl>                                                                                            | Отменить последнее действие.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**Аппкомманд \_ \_Уменьшение громкости**</dt> <dt>9</dt> </dl>                                                                       | Уменьшите объем тома.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**Аппкомманд \_ \_Отключение тома**</dt> <dt>8</dt> </dl>                                                                       | Отключите громкость.<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**Аппкомманд \_ ТОМ \_**</dt> <dt>10</dt> </dl>                                                                            | Поднимите том.<br/>                                                                                                                                                                                                                                                               |



 

Компонент *удевице* указывает устройство ввода, создавшее событие ввода, и может принимать одно из следующих значений.



| Значение                                                                                                                                                                                                                                 | Значение                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**Фаппкомманд \_ КЛЮЧ**</dt> <dt>0</dt> </dl>            | Пользователь нажал на ключ.<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**Фаппкомманд \_ МЫШЬ**</dt> <dt>0x8000</dt> </dl> | Пользователь щелкнул кнопку мыши.<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**Фаппкомманд \_ OEM**</dt> <dt>0x1000</dt> </dl>       | Неопознанный источник оборудования создал событие. Это может быть мышь или событие клавиатуры.<br/> |



 

Компонент *двкэйс* указывает, работают ли различные виртуальные ключи, и может быть одним или несколькими из следующих значений.



| Значение                                                                                                                                                                                                               | Значение                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Управление**</dt> <dt>0x0008</dt> </dl>    | Нажата клавиша CTRL.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt> </dl>    | Левая кнопка мыши не работает.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt> </dl>    | Средняя кнопка мыши не работает.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt> </dl>    | Нажата правая кнопка мыши.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | Нажата клавиша SHIFT.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | Первая кнопка X не работает.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Вторая кнопка X не работает.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**. Дополнительные сведения об обработке возвращаемого значения см. в разделе "Примечания".

## <a name="remarks"></a>Комментарии

[**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) создает сообщение **WM \_ Аппкомманд** при обработке сообщения [**WM \_ ксбуттонуп**](wm-xbuttonup.md) или [**WM \_ нкксбуттонуп**](wm-ncxbuttonup.md) или когда пользователь вводит ключ команды приложения.

Если дочернее окно не обрабатывает это сообщение и вместо этого вызывает [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), **дефвиндовпрок** отправляет сообщение в родительское окно. Если окно верхнего уровня не обрабатывает это сообщение и вместо этого вызывает **дефвиндовпрок**, **дефвиндовпрок** будет вызывать обработчик оболочки с кодом обработчика, равным **хшелл \_ аппкомманд**.

Чтобы получить координаты курсора, если сообщение было создано щелчком мыши, приложение может вызвать [**жетмессажепос**](/windows/desktop/api/winuser/nf-winuser-getmessagepos). Приложение может проверить, было ли сообщение создано с помощью мыши, проверив, содержит ли параметр *lParam* **фаппкомманд \_ Mouse**.

В отличие от других сообщений Windows, приложение должно возвращать **значение true** из этого сообщения, если оно обрабатывает его. Это позволит программному обеспечению имитировать это сообщение в системах Windows более ранних, чем Windows 2000, чтобы определить, обрабатывало ли это сообщение процедура окна или вызываемая [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) для его обработки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ПОЛУЧЕНИЕ \_ lParam для аппкомманд \_**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**ПОЛУЧЕНИЕ \_ \_ lParam устройства**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**ПОЛУЧЕНИЕ \_ lParam для кэйстате \_**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**шеллпрок**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**WM \_ ксбуттонуп**](wm-xbuttonup.md)
</dt> <dt>

[**WM \_ нкксбуттонуп**](wm-ncxbuttonup.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Ввод с помощью мыши](mouse-input.md)
</dt> </dl>

 

