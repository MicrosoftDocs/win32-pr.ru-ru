---
title: Интерфейс IMsRdpClient7
description: Предоставляет методы и свойства, необходимые для настройки и использования клиентского элемента управления. Является производным от интерфейса IMsRdpClient6.
ms.assetid: f6bc5d50-f16a-44be-8244-5aec13c52066
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, описание
topic_type:
- apiref
api_name:
- IMsRdpClient7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e16375f9f1281f2cc34dac440373f95b828392f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672919"
---
# <a name="imsrdpclient7-interface"></a>Интерфейс IMsRdpClient7

Предоставляет методы и свойства, необходимые для настройки и использования клиентского элемента управления. Является производным от интерфейса [**IMsRdpClient6**](imsrdpclient6.md) .

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClient7** наследует от [**IMsRdpClient6**](imsrdpclient6.md). **IMsRdpClient7** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **IMsRdpClient7** содержит следующие методы.



| Метод                                               | Описание                                                         |
|:-----------------------------------------------------|:--------------------------------------------------------------------|
| [**жетстатустекст**](imsrdpclient7-getstatustext.md) | Получает текст состояния для указанного кода состояния.<br/> |



 

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClient7** имеет следующие свойства.



| Свойство                                                                  | Тип доступа          | Описание                                                                                                                |
|:--------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>   | Только для чтения<br/> | Объект, который поддерживает интерфейс [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .<br/>   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>         | Только для чтения<br/> | Объект, который поддерживает интерфейс [**ITSRemoteProgram2**](itsremoteprogram2.md) .<br/>                           |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>     | Только для чтения<br/> | Объект, который поддерживает интерфейс [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .<br/>     |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/> | Только для чтения<br/> | Объект, который поддерживает интерфейс [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .<br/> |



 

## <a name="remarks"></a>Комментарии

Интерфейс **IMsRdpClient7** расширен следующими интерфейсами. каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:

-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | \_MSRDPCLIENT10 CLSID определен как C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> \_MSRDPCLIENT10NOTSAFEFORSCRIPTING CLSID определен как A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> \_MSRDPCLIENT7 CLSID определен как A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> \_MSRDPCLIENT7NOTSAFEFORSCRIPTING CLSID определен как 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> \_MSRDPCLIENT8 CLSID определен как 5F681803-2900-4C43-A1CC-CF405404A676<br/> \_MSRDPCLIENT8NOTSAFEFORSCRIPTING CLSID определен как A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> \_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> \_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient7 определен как b2a5b5ce-3461-444a-91d4-add26d070638<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

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

 

 





