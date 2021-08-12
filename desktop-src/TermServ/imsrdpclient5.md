---
title: Интерфейс IMsRdpClient5
description: Предоставляет методы и свойства, необходимые для настройки и использования клиентского элемента управления. Является производным от интерфейса IMsRdpClient4.
ms.assetid: d3fc5e67-f4d9-4d80-b572-8fc3e660571e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, описание
topic_type:
- apiref
api_name:
- IMsRdpClient5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7948d402219faa930ddc9087af1ba387bde3ce8d70752fd842a364e85b41abb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609295"
---
# <a name="imsrdpclient5-interface"></a>Интерфейс IMsRdpClient5

Предоставляет методы и свойства, необходимые для настройки и использования клиентского элемента управления. Является производным от интерфейса [**IMsRdpClient4**](imsrdpclient4.md) .

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClient5** наследует от [**IMsRdpClient4**](imsrdpclient4.md). **IMsRdpClient5** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **IMsRdpClient5** содержит следующие методы.



| Метод                                                           | Описание                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------|
| [**жетеррордескриптион**](imsrdpclient5-geterrordescription.md) | Получает коды ошибок и сообщения об ошибках.<br/> |



 

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClient5** имеет следующие свойства.



| Свойство                                                                | Тип доступа          | Описание                                                                                         |
|:------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------|
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/> | Только для чтения<br/> | Интерфейс для [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).<br/> |
| [**мсрдпклиентшелл**](imsrdpclient5-msrdpclientshell.md)<br/>   | Только для чтения<br/> | Параметры клиента для средства запуска веб-портала.<br/>                                         |
| [**ремотепрограм**](imsrdpclient5-remoteprogram.md)<br/>         | Только для чтения<br/> | Параметр клиента RemoteApp.<br/>                                                            |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/> | Только для чтения<br/> | Параметр шлюза клиентских удаленных рабочих столов.<br/>                                                           |



 

## <a name="remarks"></a>Remarks

Интерфейс **IMsRdpClient5** расширен следующими интерфейсами. каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:

-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | \_MSRDPCLIENT10 CLSID определен как C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> \_MSRDPCLIENT10NOTSAFEFORSCRIPTING CLSID определен как A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> \_MSRDPCLIENT5 CLSID определен как 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> \_MSRDPCLIENT5NOTSAFEFORSCRIPTING CLSID определен как 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> \_MSRDPCLIENT6 CLSID определен как 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> \_MSRDPCLIENT6NOTSAFEFORSCRIPTING CLSID определен как D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> \_MSRDPCLIENT7 CLSID определен как A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> \_MSRDPCLIENT7NOTSAFEFORSCRIPTING CLSID определен как 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> \_MSRDPCLIENT8 CLSID определен как 5F681803-2900-4C43-A1CC-CF405404A676<br/> \_MSRDPCLIENT8NOTSAFEFORSCRIPTING CLSID определен как A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> \_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> \_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient5 определен как 4eb5335b-6429-477d-B922-e06a28ecd8bf<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

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

 

 





