---
title: Класс Ремотедесктопклиент
description: Реализует клиентский элемент управления удаленный рабочий стол приложения для магазина Microsoft Windows — версия 1.
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов класса Ремотедесктопклиент
- Службы удаленных рабочих столов класс Ремотедесктопклиент, описание
topic_type:
- apiref
api_name:
- RemoteDesktopClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb10b23f52f53e2d89fd5a81449818a8fe374116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988389"
---
# <a name="remotedesktopclient-class"></a>Класс Ремотедесктопклиент

Реализует клиентский элемент управления для приложения Магазина Microsoft Windows удаленный рабочий стол версии 1

Этот класс реализует следующие интерфейсы.

-   [**иремотедесктопклиент**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [**иремотедесктопклиентевентс**](iremotedesktopclientevents.md)

**Ремотедесктопклиент** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **ремотедесктопклиент** содержит следующие методы.



| Метод                                                                                      | Описание                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | Присоединяет обработчик событий к событию.<br/>                                                                                                                  |
| [**Подключение**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | Инициирует соединение с использованием свойств, заданных в данный момент в контейнере клиентского приложения протокол удаленного рабочего стола (RDP).<br/>                         |
| [**делетесаведкредентиалс**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | Удаляет сохраненные учетные данные для указанного удаленного компьютера.<br/>                                                                                            |
| [**детачевент**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | Отсоединяет обработчик событий от события.<br/>                                                                                                                |
| [**Отключение**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | Отключает активное подключение.<br/>                                                                                                                      |
| [**онадминмессажерецеивед**](iremotedesktopclientevents-onadminmessagereceived.md)         | Вызывается, когда клиентский элемент управления получает административное сообщение.<br/>                                                                                      |
| [**онаутореконнектед**](iremotedesktopclientevents-onautoreconnected.md)                   | Вызывается при автоматическом повторном подключении клиентского элемента управления к удаленному сеансу.<br/>                                                                       |
| [**онаутореконнектинг**](iremotedesktopclientevents-onautoreconnecting.md)                 | Вызывается, когда клиентский элемент управления пытается автоматически восстановить соединение с удаленным сеансом.<br/>                                                  |
| [**Подключено**](iremotedesktopclientevents-onconnected.md)                               | Вызывается, когда клиентский элемент управления подключается к удаленному сеансу.<br/>                                                                                       |
| [**Подключение**](iremotedesktopclientevents-onconnecting.md)                             | Вызывается, когда клиентский элемент управления пытается установить соединение с удаленным сеансом.<br/>                                                                  |
| [**ондиалогдисмиссед**](iremotedesktopclientevents-ondialogdismissed.md)                   | Вызывается после закрытия диалогового окна, отображаемого клиентским элементом управления.<br/>                                                                                 |
| [**ондиалогдисплайинг**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Вызывается до того, как элемент управления выводит диалоговое окно.<br/>                                                                                                        |
| [**С отключением**](iremotedesktopclientevents-ondisconnected.md)                         | Вызывается, когда клиентский элемент управления был отключен от удаленного сеанса.<br/>                                                                             |
| [**онкэйкомбинатионпрессед**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Вызывается при нажатии специальных сочетаний клавиш в удаленном сеансе.<br/>                                                                                 |
| [**онлогинкомплетед**](iremotedesktopclientevents-onlogincompleted.md)                     | Вызывается, когда клиентский элемент управления успешно вошел в удаленный сеанс.<br/>                                                                          |
| [**оннетворкстатусчанжед**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Вызывается при изменении состояния сети.<br/>                                                                                                             |
| [**онремотедесктопсизечанжед**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Вызывается при изменении размера удаленного рабочего стола.<br/>                                                                                                        |
| [**онстатусчанжед**](iremotedesktopclientevents-onstatuschanged.md)                       | Вызывается, когда клиентский элемент управления обновил свое состояние.<br/>                                                                                                  |
| [**онтаучпоинтеркурсормовед**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Вызывается, когда курсор сенсорного указателя переместился и свойство [**евентсенаблед**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) имеет значение true.<br/> |
| [**Повтор соединения**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | Инициирует автоматическое повторное подключение клиентского элемента управления контейнера приложения протокол удаленного рабочего стола (RDP) в соответствии с новым шириной и высотой сеанса.<br/>   |
| [**упдатесессиондисплайсеттингс**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | Обновляет параметры ширины и высоты для клиентского элемента управления контейнера приложения протокол удаленного рабочего стола (RDP).<br/>                                               |



 

### <a name="properties"></a>Свойства

Класс **ремотедесктопклиент** имеет следующие свойства.



| Свойство                                                             | Тип доступа          | Описание                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Действия**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | Только для чтения<br/> | Извлекает объект действий для клиента контейнера приложения протокол удаленного рабочего стола (RDP).<br/>                                                                    |
| [**Параметры**](iremotedesktopclient-settings.md)<br/>         | Только для чтения<br/> | Извлекает объект параметров для клиента контейнера приложения протокол удаленного рабочего стола (RDP).<br/>                                                                   |
| [**TouchPointer**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | Только для чтения<br/> | Содержит объект [**ремотедесктопклиенттаучпоинтер**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) для клиента контейнера приложения протокол удаленного рабочего стола (RDP).<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                     |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| CLSID<br/>                    | \_РЕМОТЕДЕСКТОПКЛИЕНТ CLSID определен как EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[удаленный рабочий стол классов элементов управления ActiveX](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

