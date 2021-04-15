---
title: Интерфейс IMsRdpClient8
description: Предоставляет методы и свойства, необходимые для настройки и использования клиентского элемента управления. Является производным от интерфейса IMsRdpClient7.
ms.assetid: 5ff54392-48f2-49a9-a264-88db08ec1770
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, описание
topic_type:
- apiref
api_name:
- IMsRdpClient8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6575e50bd85cfe96888f6c5924d1875b48d544ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414777"
---
# <a name="imsrdpclient8-interface"></a>Интерфейс IMsRdpClient8

Предоставляет методы и свойства, необходимые для настройки и использования клиентского элемента управления. Является производным от интерфейса [**IMsRdpClient7**](imsrdpclient7.md) .

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClient8** наследует от [**IMsRdpClient7**](imsrdpclient7.md). **IMsRdpClient8** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **IMsRdpClient8** содержит следующие методы.



| Метод                                                                    | Описание                                                                                                                                                                                 |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Подключение**](imstscax-connect.md)                                       | Инициирует соединение с использованием свойств, заданных в данный момент в элементе управления.<br/>                                                                                                        |
| [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md)           | Создает объект виртуального канала на стороне клиента для каждого указанного имени виртуального канала.<br/>                                                                                            |
| [**Отключение**](imstscax-disconnect.md)                                 | Отключает активное подключение.<br/>                                                                                                                                               |
| [**жетеррордескриптион**](imsrdpclient5-geterrordescription.md)          | Возвращает описание ошибки для событий отключения сеанса.<br/>                                                                                                               |
| [**жетстатустекст**](imsrdpclient7-getstatustext.md)                      | Получает текст состояния для указанного кода состояния.<br/>                                                                                                                         |
| [**жетвиртуалчаннелоптионс**](imsrdpclient-getvirtualchanneloptions.md) | Извлекает параметры, заданные для виртуального канала.<br/>                                                                                                                                 |
| [**Повтор соединения**](imsrdpclient8-reconnect.md)                              | Повторно подключается к удаленному сеансу, используя новые значения ширины и высоты рабочего стола.<br/>                                                                                                          |
| [**RequestClose**](imsrdpclient-requestclose.md)                         | Запрашивает корректное завершение работы элемента управления ActiveX удаленный рабочий стол.<br/>                                                                                                              |
| [**сендонвиртуалчаннел**](imstscax-sendonvirtualchannel.md)             | Отправляет данные на сервер узла сеансов удаленных рабочих столов по виртуальному каналу, созданному ранее с помощью метода [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) .<br/> |
| [**сендремотеактион**](imsrdpclient8-sendremoteaction.md)                | Вызывает выполнение действия в удаленном сеансе.<br/>                                                                                                                          |
| [**сетвиртуалчаннелоптионс**](imsrdpclient-setvirtualchanneloptions.md) | Задает параметры виртуального канала для элемента управления ActiveX удаленный рабочий стол.<br/>                                                                                                         |



 

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClient8** имеет следующие свойства.



| Свойство                                                                             | Тип доступа           | Описание                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**адванцедсеттингс**](imstscax-advancedsettings.md)<br/>                     | Только для чтения<br/>  | Извлекает указатель интерфейса [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) .<br/>                                                                                                                                          |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Только для чтения<br/>  | Получает указатель на интерфейс [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md) . Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.<br/>                                             |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Только для чтения<br/>  | Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.<br/>                                                     |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Только для чтения<br/>  | Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .<br/>                                                                                                                                |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Только для чтения<br/>  | Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .<br/>                                                                                                                                 |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Только для чтения<br/>  | Извлекает интерфейс [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                                                             |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Только для чтения<br/>  | Извлекает интерфейс [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                                                             |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .<br/>                                                                                                                     |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Только для чтения<br/>  | Содержит объект, который поддерживает интерфейс [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .<br/>                                                                                                                      |
| [**Циферстренгс**](imstscax-cipherstrength.md)<br/>                         | Только для чтения<br/>  | Возвращает максимальную стойкость шифрования текущего элемента управления.<br/>                                                                                                                                                                           |
| [**Clientareawidth**](imsrdpclient-colordepth.md)<br/>                             | Чтение/запись<br/> | Глубина цвета (в битах на пиксель) для соединения элемента управления.<br/>                                                                                                                                                                           |
| [**Подключен**](imstscax-connected.md)<br/>                                   | Только для чтения<br/>  | Возвращает состояние соединения текущего элемента управления.<br/>                                                                                                                                                                                      |
| [**коннектедстатустекст**](imsrdpclient2-connectedstatustext.md)<br/>          | Чтение/запись<br/> | Содержит текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в подключенном состоянии.<br/>                                                                                                                          |
| [**коннектингтекст**](imstscax-connectingtext.md)<br/>                         | Чтение/запись<br/> | Задает текст, отображаемый в центре элемента управления во время подключения элемента управления.<br/>                                                                                                                                                    |
| [**десктофеигхт**](imstscax-desktopheight.md)<br/>                           | Чтение/запись<br/> | Задает высоту текущего элемента управления в пикселях на начальном удаленном рабочем столе.<br/>                                                                                                                                                           |
| [**десктопвидс**](imstscax-desktopwidth.md)<br/>                             | Чтение/запись<br/> | Задает ширину текущего элемента управления в пикселях на начальном удаленном рабочем столе.<br/>                                                                                                                                                            |
| [**дисконнектедтекст**](imstscax-disconnectedtext.md)<br/>                     | Чтение/запись<br/> | Задает текст, отображаемый по центру элемента управления до завершения соединения.<br/>                                                                                                                                                  |
| [**Домен**](imstscax-domain.md)<br/>                                         | Чтение/запись<br/> | Указывает домен, в который входит текущий пользователь.<br/>                                                                                                                                                                                     |
| [**екстендеддисконнектреасон**](imsrdpclient-extendeddisconnectreason.md)<br/> | Только для чтения<br/>  | Содержит расширенные сведения о причине отключения элемента управления.<br/>                                                                                                                                                                 |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Чтение/запись<br/> | Определяет, находится ли клиентский элемент управления в полноэкранном режиме.<br/>                                                                                                                                                                               |
| [**фуллскринтитле**](imstscax-fullscreentitle.md)<br/>                       | Только на запись<br/> | Указывает заголовок окна, отображаемый, когда элемент управления находится в полноэкранном режиме.<br/>                                                                                                                                                               |
| [**хоризонталскроллбарвисибле**](imstscax-horizontalscrollbarvisible.md)<br/> | Только для чтения<br/>  | Указывает, отображает ли элемент управления горизонтальную полосу прокрутки.<br/>                                                                                                                                                                        |
| [**мсрдпклиентшелл**](imsrdpclient5-msrdpclientshell.md)<br/>                | Только для чтения<br/>  | Получает интерфейс параметра клиента с скриптом [**имсрдпклиентшелл**](imsrdpclientshell.md).<br/>                                                                                                                                           |
| [**ремотепрограм**](imsrdpclient5-remoteprogram.md)<br/>                      | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**итсремотепрограм**](itsremoteprogram.md) .<br/>                                                                                                                                               |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**ITSRemoteProgram2**](itsremoteprogram2.md) .<br/>                                                                                                                                             |
| [**секуредсеттингс**](imstscax-securedsettings.md)<br/>                       | Только для чтения<br/>  | Извлекает указатель интерфейса [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) .<br/>                                                                                                                                            |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Только для чтения<br/>  | Получает указатель на интерфейс [**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md) . Этот интерфейс можно использовать для задания защищенных параметров клиентского элемента управления.<br/>                                               |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .<br/>                                                                                                                       |
| [**секуредсеттингсенаблед**](imstscax-securedsettingsenabled.md)<br/>         | Только для чтения<br/>  | Указывает, доступен ли интерфейс [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) . То есть, находится ли веб-страница, содержащая данный элемент управления, в одной из разрешенных зон безопасности URL-адресов Internet Explorer.<br/> |
| [**Сервером**](imstscax-server.md)<br/>                                         | Чтение/запись<br/> | Указывает имя сервера, к которому подключен текущий элемент управления.<br/>                                                                                                                                                                 |
| [**стартконнектед**](imstscax-startconnected.md)<br/>                         | Чтение/запись<br/> | Указывает, будет ли элемент управления устанавливать соединение с сервером узла сеансов удаленных рабочих столов сразу после запуска.<br/>                                                                                                                                |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Только для чтения<br/>  | Возвращает сведения о том, что было передано через скрипт в интерфейс [**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md) .<br/>                                                                                                         |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Только для чтения<br/>  | Извлекает интерфейс [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .<br/>                                                                                                                                           |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Только для чтения<br/>  | Извлекает объект, который поддерживает интерфейс [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .<br/>                                                                                                                   |
| [**Имен**](imstscax-username.md)<br/>                                     | Чтение/запись<br/> | Указывает учетные данные имени пользователя для входа.<br/>                                                                                                                                                                                                   |
| [**Версия**](imstscax-version.md)<br/>                                       | Только для чтения<br/>  | Указывает номер версии текущего элемента управления.<br/>                                                                                                                                                                                        |
| [**вертикалскроллбарвисибле**](imstscax-verticalscrollbarvisible.md)<br/>     | Только для чтения<br/>  | Указывает, отображает ли элемент управления вертикальную полосу прокрутки.<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Комментарии

Интерфейс **IMsRdpClient8** расширен следующими интерфейсами. каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:

-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID<br/>                    | \_MSRDPCLIENT10 CLSID определен как C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> \_MSRDPCLIENT10NOTSAFEFORSCRIPTING CLSID определен как A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> \_MSRDPCLIENT8 CLSID определен как 5F681803-2900-4C43-A1CC-CF405404A676<br/> \_MSRDPCLIENT8NOTSAFEFORSCRIPTING CLSID определен как A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> \_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> \_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient8 определен как 4247E044-9271-43A9-BC49-E2AD9E855D62<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

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

 

 





