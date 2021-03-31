---
title: Класс MsRdpClient8
description: Клиентский элемент управления Microsoft RDP (распространяемый пакет) — версия 9.
ms.assetid: 877D475B-E2B4-46FB-B7A1-D376F6AE6B8D
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов класса MsRdpClient8
- Службы удаленных рабочих столов класс MsRdpClient8, описание
topic_type:
- apiref
api_name:
- MsRdpClient8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc1410df2be1b738d217372a563cfdef13cbc3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988393"
---
# <a name="msrdpclient8-class"></a>Класс MsRdpClient8

Клиентский элемент управления Microsoft RDP (распространяемый пакет) — версия 9

Этот класс реализует следующие интерфейсы.

-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**имсрдпклиент**](imsrdpclientshell2.md)
-   [**имстскакс**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**имстскаксевентс**](imstscaxevents-interface.md)
-   [**имстскнонскриптабле**](imstscnonscriptable-interface.md)
-   [**имсрдпклиентнонскриптабле**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
-   [**имсрдппреферредредиректионинфо**](imsrdppreferredredirectioninfo.md)

**MsRdpClient8** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **MsRdpClient8** содержит следующие методы.



| Метод                                                                                      | Описание                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Подключение**](imstscax-connect.md)                                                         | Инициирует соединение с использованием свойств, заданных в данный момент в элементе управления.<br/>                                                                                                                                                                                                          |
| [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md)                             | Создает объект виртуального канала на стороне клиента для каждого указанного имени виртуального канала.<br/>                                                                                                                                                                                              |
| [**Отключение**](imstscax-disconnect.md)                                                   | Отключает активное подключение.<br/>                                                                                                                                                                                                                                                 |
| [**жетеррордескриптион**](imsrdpclient5-geterrordescription.md)                            | Получает коды ошибок и сообщения об ошибках.<br/>                                                                                                                                                                                                                                      |
| [**жетстатустекст**](imsrdpclient7-getstatustext.md)                                        | Получает текст состояния для указанного кода состояния.<br/>                                                                                                                                                                                                                           |
| [**жетвиртуалчаннелоптионс**](imsrdpclient-getvirtualchanneloptions.md)                   | Извлекает параметры, заданные для виртуального канала.<br/>                                                                                                                                                                                                                                   |
| [**нотифиредиректдевицечанже**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Уведомляет модуль перенаправления устройств элемента управления ActiveX удаленный рабочий стол, что в системе произошло изменение устройства. Этот метод передает в элемент управления уведомления [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) .<br/>                                                        |
| [**онаусентикатионварнингдисмиссед**](imstscaxevents-onauthenticationwarningdismissed.md) | Вызывается после того, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "Ошибка сертификата").<br/>                                                                                                                                                             |
| [**онаусентикатионварнингдисплайед**](imstscaxevents-onauthenticationwarningdisplayed.md) | Вызывается перед тем, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "Ошибка сертификата").<br/>                                                                                                                                                            |
| [**онаутореконнектед**](imstscaxevents-onautoreconnected.md)                               | Вызывается при автоматическом повторном подключении клиентского элемента управления к удаленному сеансу.<br/>                                                                                                                                                                                                  |
| [**онаутореконнектинг**](-imstscaxevents--onautoreconnecting.md)                           | Вызывается, когда клиент находится в процессе автоматического повторного подключения к сеансу с сервером узла сеансов удаленных рабочих столов.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Вызывается, когда клиент находится в процессе автоматического повторного подключения к сеансу с сервером узла сеансов удаленных рабочих столов.<br/>                                                                                                                                                                      |
| [**ончаннелрецеиведдата**](imstscaxevents-onchannelreceiveddata.md)                       | Вызывается, когда клиент получает данные в виртуальном канале, поддерживающем скрипт.<br/>                                                                                                                                                                                                              |
| [**онконфирмклосе**](imstscaxevents-onconfirmclose.md)                                     | Вызывается, когда клиент вызывает метод [**имсрдпклиент:: RequestClose**](imsrdpclient-requestclose.md) .<br/>                                                                                                                                                                           |
| [**Подключено**](imstscaxevents-onconnected.md)                                           | Вызывается, когда клиентский элемент управления находится в процессе установления соединения с сервером узла сеансов удаленных рабочих столов.<br/>                                                                                                                                                                       |
| [**Подключение**](imstscaxevents-onconnecting.md)                                         | Вызывается, когда клиентский элемент управления начинает подключаться к серверу в ответ на вызов [**имстскакс:: Connect**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**онконнектионбарпуллдовн**](imstscaxevents-onconnectionbarpulldown.md)                   | Вызывается, когда пользователь перетаскивается на панель подключения.<br/>                                                                                                                                                                                                                       |
| [**ондевицесбуттонпрессед**](imstscaxevents-ondevicesbuttonpressed.md)                     | Вызывается при нажатии кнопки устройства на панели подключения.<br/>                                                                                                                                                                                                             |
| [**С отключением**](imstscaxevents-ondisconnected.md)                                     | Вызывается, когда клиентский элемент управления был отключен от сервера узла сеансов удаленных рабочих столов.<br/>                                                                                                                                                                                              |
| [**онентерфуллскринмоде**](imstscaxevents-onenterfullscreenmode.md)                       | Вызывается, когда клиент переходит в полноэкранный режим. Например, это событие вызывается при нажатии [пользователем сочетания клавиш](terminal-services-shortcut-keys.md) в полноэкранном режиме (Ctrl + Alt + Break).<br/>                                                                     |
| [**онфаталеррор**](imstscaxevents-onfatalerror.md)                                         | Вызывается, когда клиентский элемент управления обнаруживает неустранимую ошибку.<br/>                                                                                                                                                                                                                           |
| [**онфокусрелеасед**](imstscaxevents-onfocusreleased.md)                                   | Вызывается при нажатии сочетания клавиш для фокуса в выпуске. Например, это событие вызывается, когда пользователь нажимает клавишу CTRL + ALT + стрелка влево или сочетание клавиш CTRL + ALT + стрелка вправо.<br/>                                                                                             |
| [**онидлетимеаутнотификатион**](imstscaxevents-onidletimeoutnotification.md)               | Вызывается, когда пользователь не наводит мышь или клавиатуру в течение периода времени, заданного методом [**имсрдпклиентадванцедсеттингс::p UT \_ минутестоидлетимеаут**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .<br/>                                                |
| [**онлеавефуллскринмоде**](imstscaxevents-onleavefullscreenmode.md)                       | Вызывается, когда клиент выходит из полноэкранного режима. Например, это событие вызывается при нажатии [пользователем сочетания клавиш](terminal-services-shortcut-keys.md) в полноэкранном режиме (Ctrl + Alt + Break).<br/>                                                                     |
| [**онлогинкомплете**](imstscaxevents-onlogincomplete.md)                                   | Вызывается, когда клиентский элемент управления успешно выполнил вход на сервер узла сеансов удаленных рабочих столов, следуя отображаемому в диалоговом окне входа в систему.<br/>                                                                                                                                      |
| [**онлогонеррор**](imstscaxevents-onlogonerror.md)                                         | Вызывается при возникновении ошибки входа в систему или другого события входа.<br/>                                                                                                                                                                                                                             |
| [**онмаусеинпутмодечанжед**](imstscaxevents-onmouseinputmodechanged.md)                   | Вызывается при изменении режима ввода с помощью мыши.<br/>                                                                                                                                                                                                                                      |
| [**оннетворкстатусчанжед**](imstscaxevents-onnetworkstatuschanged.md)                     | Вызывается при изменении состояния сети.<br/>                                                                                                                                                                                                                                        |
| [**онрецеиведтспубликкэй**](imstscaxevents-onreceivedtspublickey.md)                       | Вызывается во время последовательности подключения, когда клиент получает открытый ключ с сервера. Это событие вызывается, только если свойство **нотифитспубликкэй** имеет значение **Variant \_ true**.<br/>                                                                                              |
| [**онремотедесктопсизечанже**](imstscaxevents-onremotedesktopsizechange.md)               | Вызывается для указания того, что размер клиентского элемента управления в удаленном рабочем столе изменился в ответ на операцию клиентского управления.<br/>                                                                                                                                                |
| [**онремотепрограмдисплайед**](imstscaxevents-onremoteprogramdisplayed.md)                 | Вызывается при отображении программы RemoteApp.<br/>                                                                                                                                                                                                                                      |
| [**онремотепрограмресулт**](imstscaxevents-onremoteprogramresult.md)                       | Вызывается, когда программа RemoteApp возвращает результат в клиентский элемент управления.<br/>                                                                                                                                                                                                            |
| [**онремотевиндовдисплайед**](imstscaxevents-onremotewindowdisplayed.md)                   | Вызывается при отображении окна RemoteApp.<br/>                                                                                                                                                                                                                                       |
| [**онрекуестконтаинерминимизе**](imstscaxevents-onrequestcontainerminimize.md)             | Вызывается, когда пользователь нажимает кнопку **сворачивания** на панели подключения в полноэкранном режиме. Срабатывание этого события является запрос, в котором приложение контейнера свернется само по себе.<br/>                                                                                              |
| [**онрекуестгофуллскрин**](imstscaxevents-onrequestgofullscreen.md)                       | Вызывается, когда клиент запрашивает переключение в полноэкранный режим и вызывается метод [**имстскадванцедсеттингс::p UT \_ контаинерхандледфуллскрин**](imstscadvancedsettings-containerhandledfullscreen.md) , чтобы установить свойство **контаинерхандледфуллскрин** в ненулевое значение.<br/> |
| [**онрекуестлеавефуллскрин**](imstscaxevents-onrequestleavefullscreen.md)                 | Вызывается, когда клиент запрашивает, чтобы выйти из полноэкранного режима, а свойство [**имстскадванцедсеттингс::p UT \_ контаинерхандледфуллскрин**](imstscadvancedsettings-containerhandledfullscreen.md) установлено в ненулевое значение.<br/>                                                   |
| [**онсервицемессажерецеивед**](imstscaxevents-onservicemessagereceived.md)                 | Вызывается, когда клиент получает системное сообщение.<br/>                                                                                                                                                                                                                                  |
| [**онусернамеаккуиред**](imstscaxevents-onusernameacquired.md)                             | Вызывается, когда имя пользователя было получено элементом управления.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Вызывается, когда клиентский элемент управления обнаруживает неустранимое условие ошибки.<br/>                                                                                                                                                                                                    |
| [**Повтор соединения**](imsrdpclient8-reconnect.md)                                                | Повторно подключается к удаленному сеансу, используя новые значения ширины и высоты рабочего стола.<br/>                                                                                                                                                                                                            |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Запрашивает корректное завершение работы клиентского элемента управления.<br/>                                                                                                                                                                                                                                |
| [**ресетпассворд**](imstscnonscriptable-resetpassword.md)                                  | Сбрасывает все состояния паролей в элементе управления.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Отправляет в элемент управления ряд нажатий клавиш. Нажатия клавиш находятся в форме кода сканирования, которая является данными клавиатуры из фактических физических ключей.<br/>                                                                                                                                       |
| [**сендонвиртуалчаннел**](imstscax-sendonvirtualchannel.md)                               | Отправляет данные на сервер узла сеансов удаленных рабочих столов по виртуальному каналу, созданному ранее с помощью метода [**имстскакс:: креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) .<br/>                                                                                         |
| [**сендремотеактион**](imsrdpclient8-sendremoteaction.md)                                  | Вызывает выполнение действия в удаленном сеансе.<br/>                                                                                                                                                                                                                            |
| [**сетвиртуалчаннелоптионс**](imsrdpclient-setvirtualchanneloptions.md)                   | Задает параметры виртуального канала для клиентского элемента управления.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Свойства

Класс **MsRdpClient8** имеет следующие свойства.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Свойство</th>
<th style="text-align: left;">Тип доступа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-advancedsettings.md"><strong>адванцедсеттингс</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указатель интерфейса <a href="imstscadvancedsettings-interface.md"><strong>имстскадванцедсеттингс</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указатель на интерфейс <a href="imsrdpclientadvancedsettings-interface.md"><strong>имсрдпклиентадванцедсеттингс</strong></a> , используемый для задания дополнительных параметров клиентского элемента управления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указатель на интерфейс <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2</strong></a> , используемый для задания дополнительных параметров клиентского элемента управления.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указатель на интерфейс <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3</strong></a> , используемый для задания дополнительных параметров клиентского элемента управления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указатель интерфейса <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Интерфейс для <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient6-advancedsettings7.md"><strong>AdvancedSettings7</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Интерфейс для <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-advancedsettings8.md"><strong>AdvancedSettings8</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Объект, который поддерживает интерфейс <a href="imsrdpclientadvancedsettings7.md"><strong>IMsRdpClientAdvancedSettings7</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient8-advancedsettings9.md"><strong>AdvancedSettings9</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Интерфейс <a href="imsrdpclientadvancedsettings8.md"><strong>IMsRdpClientAdvancedSettings8</strong></a> , представляющий объект Settings.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>алловкредентиалсавинг</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, отображает ли диалоговое окно учетные данные флажок для включения сохранения учетных данных.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-allowpromptingforcredentials.md"><strong>алловпромптингфоркредентиалс</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, может ли элемент управления удаленный рабочий стол ActiveX запрашивать учетные данные у пользователя.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-binarypassword.md"><strong>бинарипассворд</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Данное свойство не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-binarysalt.md"><strong>бинарисалт</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Данное свойство не поддерживается.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-cipherstrength.md"><strong>Циферстренгс</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Максимальная стойкость шифрования текущего элемента управления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-cleartextpassword.md"><strong>клеартекстпассворд</strong></a><br/></td>
<td style="text-align: left;">Только на запись<br/></td>
<td style="text-align: left;">Удаленный рабочий стол пароль элемента управления ActiveX в текстовом формате.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-colordepth.md"><strong>Clientareawidth</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Глубина цвета текущего элемента управления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connected.md"><strong>Подключен</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Состояние соединения текущего элемента управления.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient2-connectedstatustext.md"><strong>коннектедстатустекст</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в состоянии Connected.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connectingtext.md"><strong>коннектингтекст</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Текст, отображаемый по центру элемента управления во время подключения элемента управления.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>коннектионбартекст</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Текстовая строка, отображаемая для панели подключения.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-desktopheight.md"><strong>десктофеигхт</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Высота текущего элемента управления (в пикселях) на начальном удаленном рабочем столе.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-desktopwidth.md"><strong>десктопвидс</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Ширина текущего элемента управления (в пикселях) на начальном удаленном рабочем столе.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>Описания</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Коллекция устройств PnP, доступных для перенаправления.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableconnectionbar.md"><strong>дисаблеконнектионбар</strong></a><br/></td>
<td style="text-align: left;">Только на запись<br/></td>
<td style="text-align: left;">Указывает, должен ли элемент управления ActiveX удаленный рабочий стол отключать панель подключения.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableremoteappcapscheck.md"><strong>дисаблеремотеаппкапсчекк</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, должен ли элемент управления ActiveX удаленный рабочий стол не проверять наличие у сервера возможностей RemoteApp.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-disconnectedtext.md"><strong>дисконнектедтекст</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Текст, отображаемый по центру элемента управления до завершения соединения.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-domain.md"><strong>Домен</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Домен, в который входит текущий пользователь.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>дривеколлектион</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Коллекция дисков, доступная для перенаправления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>енаблекредсспсуппорт</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, включен ли CredSSP для этого соединения.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-extendeddisconnectreason.md"><strong>екстендеддисконнектреасон</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Расширенные сведения о причине отключения клиентского элемента управления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-fullscreen.md"><strong>FullScreen</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, находится ли элемент управления в полноэкранном режиме.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-fullscreentitle.md"><strong>фуллскринтитле</strong></a><br/></td>
<td style="text-align: left;">Только на запись<br/></td>
<td style="text-align: left;">Заголовок окна, отображаемый, если элемент управления находится в полноэкранном режиме.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md"><strong>жетремотемониторсбаундингбокс</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Задает ограничивающий прямоугольник удаленного монитора.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-horizontalscrollbarvisible.md"><strong>хоризонталскроллбарвисибле</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указывает, отображает ли элемент управления горизонтальную полосу прокрутки.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>лаунчедвиаклиентшеллинтерфаце</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, запустил ли пользователь клиентский элемент управления с помощью интерфейса Веб-доступ удаленных рабочих столов.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>маркрдпсеттингссекуре</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, помечены ли параметры RDP как безопасные.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-msrdpclientshell.md"><strong>мсрдпклиентшелл</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Параметры клиента для средства запуска веб-портала.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>неготиатесекуритилайер</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, поддерживается ли параметр Неготиатесекуритилайер для этого соединения.<br/>
<blockquote>
[!Note]<br />
Если <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>кредсспсуппорт</strong></a> включен и находится на клиенте или если SSL (SSL) включен с проверкой подлинности пользователя, неготиатесекуритилайер игнорируется.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-portablepassword.md"><strong>портаблепассворд</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Данное свойство не поддерживается.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-portablesalt.md"><strong>портаблесалт</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Данное свойство не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>промптфоркредентиалс</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, следует ли отображать диалоговое окно Запрос учетных данных.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>промптфоркредсонклиент</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, отображает ли клиентский элемент управления диалоговое окно с запросом учетных данных.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>публишерцертификатечаин</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает цепочку сертификатов издателя. Цепочка хранится в варианте типа VT_BYREF, который содержит указатель на структуру <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>редиректдинамикдевицес</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, доступны ли для перенаправления динамически подключаемые устройства PnP, перечисленные в сеансе.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>редиректдинамикдривес</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, доступны ли для перенаправления динамически подключаемые диски PnP, перечисленные в сеансе.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>редиректионварнингтипе</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Управляет присутствием и внешним видом диалогового окна перенаправления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorcount.md"><strong>ремотемониторкаунт</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указывает число удаленных мониторов.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md"><strong>ремотемониторлайаутматчеслокал</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указывает, идентичен ли макет удаленного монитора структуре локального монитора.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-remoteprogram.md"><strong>ремотепрограм</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Параметр клиента RemoteApp.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-remoteprogram2.md"><strong>RemoteProgram2</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Объект, который поддерживает интерфейс <a href="itsremoteprogram2.md"><strong>ITSRemoteProgram2</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-securedsettings.md"><strong>секуредсеттингс</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указатель интерфейса <a href="imstscsecuredsettings-interface.md"><strong>имстсксекуредсеттингс</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указатель на интерфейс <a href="imsrdpclientsecuredsettings-interface.md"><strong>имсрдпклиентсекуредсеттингс</strong></a> , используемый для задания защищенных параметров клиентского элемента управления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient7-securedsettings3.md"><strong>SecuredSettings3</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Объект, который поддерживает интерфейс <a href="imsrdpclientsecuredsettings2.md"><strong>IMsRdpClientSecuredSettings2</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-securedsettingsenabled.md"><strong>секуредсеттингсенаблед</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указывает, доступен ли интерфейс <a href="imstscsecuredsettings-interface.md"><strong>имстсксекуредсеттингс</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-server.md"><strong>Сервером</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Имя сервера, к которому подключен текущий элемент управления.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>шовредиректионварнингдиалог</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, следует ли отображать диалоговое окно предупреждения безопасности перенаправления перед запуском сеанса.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-startconnected.md"><strong>стартконнектед</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, будет ли элемент управления устанавливать соединение с сервером узла сеансов удаленных рабочих столов сразу после запуска.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Параметр шлюза клиентских удаленных рабочих столов.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Интерфейс для <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-transportsettings3.md"><strong>TransportSettings3</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Объект, который поддерживает интерфейс <a href="imsrdpclienttransportsettings3.md"><strong>IMsRdpClientTransportSettings3</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>трустедзонесите</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, находится ли веб-сайт, с которого пользователь запустил подключение, в списке надежных сайтов клиентского компьютера.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>уипарентвиндовхандле</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Маркер окна, который будет родительским окном для элемента управления. Это позволяет корректно модальным окнам, отображаемым элементом управления, по отношению к любым окнам, отображаемым родительским приложением.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-usemultimon.md"><strong>усемултимон</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, должен ли элемент управления ActiveX удаленный рабочий стол использовать несколько мониторов.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>усередиректионсервернаме</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, следует ли использовать имя сервера перенаправления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-username.md"><strong>Имен</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Учетные данные имени пользователя для входа.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-version.md"><strong>Версия</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Номер версии текущего элемента управления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-verticalscrollbarvisible.md"><strong>вертикалскроллбарвисибле</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Указывает, отображает ли элемент управления вертикальную полосу прокрутки.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>варнабаутклипбоардредиректион</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, должно ли диалоговое окно "предупреждение системы безопасности" включать предупреждение о перенаправлении буфера обмена перед запуском сеанса.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-warnaboutdirectxredirection.md"><strong>варнабаутдиректксредиректион</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Это свойство не используется.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>варнабаутпринтерредиректион</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, отображается ли в диалоговом окне перенаправление сообщение о перенаправлении принтера перед запуском сеанса.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>варнабаутсендингкредентиалс</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Указывает, должно ли предупреждение безопасности включать предупреждение об отправке учетных данных на удаленный сервер перед запуском сеанса.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | \_MSRDPCLIENT8 CLSID определен как 5F681803-2900-4C43-A1CC-CF405404A676<br/>      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[удаленный рабочий стол классов элементов управления ActiveX](remote-desktop-activex-control-classes.md)
</dt> </dl>

