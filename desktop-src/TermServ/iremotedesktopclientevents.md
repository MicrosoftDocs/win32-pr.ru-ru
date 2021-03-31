---
title: Интерфейс Иремотедесктопклиентевентс
description: Предоставляет методы, получающие от сервера сведения, связанные с событиями клиентского элемента управления.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, описание
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071627"
---
# <a name="iremotedesktopclientevents-interface"></a>Интерфейс Иремотедесктопклиентевентс

Предоставляет методы, получающие от сервера сведения, связанные с событиями клиентского элемента управления. К событиям относятся подключение и отключение, запросы в полноэкранном режиме, успешный вход и условия ошибки.

## <a name="members"></a>Элементы

Интерфейс **иремотедесктопклиентевентс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иремотедесктопклиентевентс** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иремотедесктопклиентевентс** содержит следующие методы.



| Метод                                                                                      | Описание                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**онадминмессажерецеивед**](iremotedesktopclientevents-onadminmessagereceived.md)         | Вызывается, когда клиентский элемент управления получает административное сообщение. <br/>                                                                                      |
| [**онаутореконнектед**](iremotedesktopclientevents-onautoreconnected.md)                   | Вызывается при автоматическом повторном подключении клиентского элемента управления к удаленному сеансу. <br/>                                                                       |
| [**онаутореконнектинг**](iremotedesktopclientevents-onautoreconnecting.md)                 | Вызывается, когда клиентский элемент управления пытается автоматически восстановить соединение с удаленным сеансом. <br/>                                                  |
| [**Подключено**](iremotedesktopclientevents-onconnected.md)                               | Вызывается, когда клиентский элемент управления подключается к удаленному сеансу.<br/>                                                                                        |
| [**Подключение**](iremotedesktopclientevents-onconnecting.md)                             | Вызывается, когда клиентский элемент управления пытается установить соединение с удаленным сеансом. <br/>                                                                  |
| [**ондиалогдисмиссед**](iremotedesktopclientevents-ondialogdismissed.md)                   | Вызывается после закрытия диалогового окна, отображаемого клиентским элементом управления. <br/>                                                                                 |
| [**ондиалогдисплайинг**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Вызывается до того, как элемент управления выводит диалоговое окно. <br/>                                                                                                        |
| [**С отключением**](iremotedesktopclientevents-ondisconnected.md)                         | Вызывается, когда клиентский элемент управления был отключен от удаленного сеанса. <br/>                                                                             |
| [**онкэйкомбинатионпрессед**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Вызывается при нажатии специальных сочетаний клавиш в удаленном сеансе. <br/>                                                                                 |
| [**онлогинкомплетед**](iremotedesktopclientevents-onlogincompleted.md)                     | Вызывается, когда клиентский элемент управления успешно вошел в удаленный сеанс. <br/>                                                                          |
| [**оннетворкстатусчанжед**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Вызывается при изменении состояния сети. <br/>                                                                                                             |
| [**онремотедесктопсизечанжед**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Вызывается при изменении размера удаленного рабочего стола. <br/>                                                                                                        |
| [**онстатусчанжед**](iremotedesktopclientevents-onstatuschanged.md)                       | Вызывается, когда клиентский элемент управления обновил свое состояние. <br/>                                                                                                  |
| [**онтаучпоинтеркурсормовед**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Вызывается, когда курсор сенсорного указателя переместился и свойство [**евентсенаблед**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) имеет значение true. <br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                           |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                 |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| CLSID<br/>                    | \_РЕМОТЕДЕСКТОПКЛИЕНТ CLSID определен как EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/>       |
| IID<br/>                      | ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по элементу управления ActiveX удаленный рабочий стол](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

