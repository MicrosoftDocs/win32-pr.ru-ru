---
title: Интерфейс IMsRdpClient10
description: Предоставляет методы и свойства, необходимые для настройки и использования клиентского элемента управления. Является производным от интерфейса IMsRdpClient9.
ms.assetid: 601f70aa-85f1-4180-921b-9f1bb31d4def
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, описание
topic_type:
- apiref
api_name:
- IMsRdpClient10
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5992803a04a771aed716251bd25ca2eceb9f94d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415072"
---
# <a name="imsrdpclient10-interface"></a>Интерфейс IMsRdpClient10

Предоставляет методы и свойства, необходимые для настройки и использования клиентского элемента управления. Является производным от интерфейса [**IMsRdpClient9**](imsrdpclient9.md) .

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClient10** наследует от [**IMsRdpClient9**](imsrdpclient9.md). **IMsRdpClient10** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **IMsRdpClient10** содержит следующие методы.



| Метод                                                                             | Описание                                                                         |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                   | Присоединяет событие.<br/>                                                       |
| [**детачевент**](imsrdpclient9-detachevent.md)                                   | Отсоединяет событие.<br/>                                                       |
| [**жетеррордескриптион**](imsrdpclient5-geterrordescription.md)                   | Возвращает описание ошибки для событий отключения сеанса.<br/>       |
| [**жетстатустекст**](imsrdpclient7-getstatustext.md)                               | Получает текст состояния для указанного кода состояния.<br/>                 |
| [**жетвиртуалчаннелоптионс**](imsrdpclient-getvirtualchanneloptions.md)          | Извлекает параметры, заданные для виртуального канала.<br/>                         |
| [**Повтор соединения**](imsrdpclient8-reconnect.md)                                       | Повторно подключается к удаленному сеансу, используя новые значения ширины и высоты рабочего стола.<br/>  |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Запрашивает корректное завершение работы элемента управления ActiveX удаленный рабочий стол.<br/>      |
| [**сендремотеактион**](imsrdpclient8-sendremoteaction.md)                         | Вызывает выполнение действия в удаленном сеансе.<br/>                  |
| [**сетвиртуалчаннелоптионс**](imsrdpclient-setvirtualchanneloptions.md)          | Задает параметры виртуального канала для элемента управления ActiveX удаленный рабочий стол.<br/> |
| [**синксессиондисплайсеттингс**](imsrdpclient9-syncsessiondisplaysettings.md)     | Синхронизирует параметры дисплея сеанса.<br/>                                   |
| [**упдатесессиондисплайсеттингс**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Обновляет параметры вывода сеанса.<br/>                                        |



 

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClient10** имеет следующие свойства.



| Свойство                                                                             | Тип доступа           | Описание                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Только для чтения<br/>  | Получает указатель на интерфейс [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md) . Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Только для чтения<br/>  | Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Только для чтения<br/>  | Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .<br/>                                                                                    |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Только для чтения<br/>  | Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .<br/>                                                                                     |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Только для чтения<br/>  | Извлекает интерфейс [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                 |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Только для чтения<br/>  | Извлекает интерфейс [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                 |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .<br/>                                                                         |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Только для чтения<br/>  | Содержит объект, который поддерживает интерфейс [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .<br/>                                                                          |
| [**Clientareawidth**](imsrdpclient-colordepth.md)<br/>                             | Чтение/запись<br/> | Глубина цвета (в битах на пиксель) для соединения элемента управления.<br/>                                                                                                                               |
| [**коннектедстатустекст**](imsrdpclient2-connectedstatustext.md)<br/>          | Чтение/запись<br/> | Содержит текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в подключенном состоянии.<br/>                                                                              |
| [**екстендеддисконнектреасон**](imsrdpclient-extendeddisconnectreason.md)<br/> | Только для чтения<br/>  | Содержит расширенные сведения о причине отключения элемента управления.<br/>                                                                                                                     |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Чтение/запись<br/> | Определяет, находится ли клиентский элемент управления в полноэкранном режиме.<br/>                                                                                                                                   |
| [**мсрдпклиентшелл**](imsrdpclient5-msrdpclientshell.md)<br/>                | Только для чтения<br/>  | Получает интерфейс параметра клиента с скриптом [**имсрдпклиентшелл**](imsrdpclientshell.md).<br/>                                                                                               |
| [**ремотепрограм**](imsrdpclient5-remoteprogram.md)<br/>                      | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**итсремотепрограм**](itsremoteprogram.md) .<br/>                                                                                                   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**ITSRemoteProgram2**](itsremoteprogram2.md) .<br/>                                                                                                 |
| [**RemoteProgram3**](imsrdpclient10-remoteprogram3.md)<br/>                   | Только для чтения<br/>  | Объект, который поддерживает интерфейс [**ITSRemoteProgram3**](itsremoteprogram3.md) .<br/>                                                                                                           |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Только для чтения<br/>  | Получает указатель на интерфейс [**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md) . Этот интерфейс можно использовать для задания защищенных параметров клиентского элемента управления.<br/>   |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .<br/>                                                                           |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Только для чтения<br/>  | Возвращает сведения о том, что было передано через скрипт в интерфейс [**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md) .<br/>                                                             |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Только для чтения<br/>  | Извлекает интерфейс [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .<br/>                                                                                               |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .<br/>                                                                       |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .<br/>                                                                       |



 

## <a name="remarks"></a>Комментарии

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                                                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                                                                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| CLSID<br/>                    | \_MSRDPCLIENT10 CLSID определен как C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> \_MSRDPCLIENT10NOTSAFEFORSCRIPTING CLSID определен как A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> |
| IID<br/>                      | IID \_ IMsRdpClient10 определен как 7ED92C39-EB38-4927-A70A-708AC5A59321<br/>                                                                                                        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**имсрдпклиент**](imsrdpclient-interface.md)
</dt> <dt>

[**имстскакс**](imstscax-interface.md)
</dt> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

