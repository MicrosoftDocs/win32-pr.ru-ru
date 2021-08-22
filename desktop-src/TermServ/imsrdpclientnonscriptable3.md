---
title: Интерфейс IMsRdpClientNonScriptable3
description: предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса IMsRdpClientNonScriptable2.
ms.assetid: 40cfcd8e-5dd7-497d-8c57-da1f542136b8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, описание
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65756224134392629a11cc0bbe2ef35f8d687cc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474560"
---
# <a name="imsrdpclientnonscriptable3-interface"></a>Интерфейс IMsRdpClientNonScriptable3

предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) . Доступ к методам этого интерфейса возможен только через таблицу vtable; они недоступны для использования в сценариях клиентов.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientNonScriptable3** наследует от [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md). **IMsRdpClientNonScriptable3** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **IMsRdpClientNonScriptable3** имеет следующие свойства.




| Свойство | Тип доступа | Описание | 
|----------|-------------|-------------|
| <a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>коннектионбартекст</strong></a><br /> | Чтение/запись<br /> | Текстовая строка, отображаемая для панели подключения.<br /> | 
| <a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>Описания</strong></a><br /> | Только для чтения<br /> | Коллекция устройств PnP, доступных для перенаправления.<br /> | 
| <a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>дривеколлектион</strong></a><br /> | Только для чтения<br /> | Коллекция дисков, доступная для перенаправления.<br /> | 
| <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>енаблекредсспсуппорт</strong></a><br /> | Чтение/запись<br /> | Указывает, включен ли CredSSP для этого соединения.<br /> | 
| <a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>неготиатесекуритилайер</strong></a><br /> | Чтение/запись<br /> | Указывает, поддерживается ли параметр Неготиатесекуритилайер для этого соединения.<br /><blockquote>[!Note]<br />Если <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>кредсспсуппорт</strong></a> включен и находится на клиенте или если SSL (SSL) включен с проверкой подлинности пользователя, неготиатесекуритилайер игнорируется.</blockquote><br /> | 
| <a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>промптфоркредентиалс</strong></a><br /> | Чтение/запись<br /> | Указывает, следует ли отображать диалоговое окно Запрос учетных данных.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>редиректдинамикдевицес</strong></a><br /> | Чтение/запись<br /> | Указывает, доступны ли для перенаправления динамически подключаемые устройства PnP, перечисленные в сеансе.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>редиректдинамикдривес</strong></a><br /> | Чтение/запись<br /> | Указывает, доступны ли для перенаправления динамически подключаемые диски PnP, перечисленные в сеансе.<br /> | 
| <a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>шовредиректионварнингдиалог</strong></a><br /> | Чтение/запись<br /> | Указывает, следует ли отображать диалоговое окно предупреждения безопасности перенаправления перед запуском сеанса.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>варнабаутклипбоардредиректион</strong></a><br /> | Чтение/запись<br /> | Указывает, должно ли диалоговое окно "предупреждение системы безопасности" включать предупреждение о перенаправлении буфера обмена перед запуском сеанса.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>варнабаутсендингкредентиалс</strong></a><br /> | Чтение/запись<br /> | Указывает, должно ли предупреждение безопасности включать предупреждение об отправке учетных данных на удаленный сервер перед запуском сеанса.<br /> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | \_MSRDPCLIENT10 CLSID определен как C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> \_MSRDPCLIENT10NOTSAFEFORSCRIPTING CLSID определен как A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> \_MSRDPCLIENT5 CLSID определен как 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> \_MSRDPCLIENT5NOTSAFEFORSCRIPTING CLSID определен как 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> \_MSRDPCLIENT6 CLSID определен как 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> \_MSRDPCLIENT6NOTSAFEFORSCRIPTING CLSID определен как D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> \_MSRDPCLIENT7 CLSID определен как A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> \_MSRDPCLIENT7NOTSAFEFORSCRIPTING CLSID определен как 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> \_MSRDPCLIENT8 CLSID определен как 5F681803-2900-4C43-A1CC-CF405404A676<br/> \_MSRDPCLIENT8NOTSAFEFORSCRIPTING CLSID определен как A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> \_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> \_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**имсрдпклиентнонскриптабле**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**имстскнонскриптабле**](imstscnonscriptable-interface.md)
</dt> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





