---
title: Интерфейс IMsRdpClientNonScriptable4
description: Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса IMsRdpClientNonScriptable3.
ms.assetid: 570a5722-94b9-4195-846a-10233d56002d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, описание
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aedea56733a2a98db4b966bd91d9337e38e61d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989413"
---
# <a name="imsrdpclientnonscriptable4-interface"></a>Интерфейс IMsRdpClientNonScriptable4

Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md) . Доступ к методам этого интерфейса возможен только через таблицу vtable; они недоступны для использования в сценариях клиентов.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientNonScriptable4** наследует от [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md). **IMsRdpClientNonScriptable4** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClientNonScriptable4** имеет следующие свойства.



| Свойство                                                                                                         | Тип доступа           | Описание                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**алловкредентиалсавинг**](imsrdpclientnonscriptable4-allowcredentialsaving.md)<br/>                     | Чтение/запись<br/> | Указывает, отображает ли диалоговое окно учетные данные флажок для включения сохранения учетных данных.<br/>                                                                                        |
| [**лаунчедвиаклиентшеллинтерфаце**](imsrdpclientnonscriptable4-launchedviaclientshellinterface.md)<br/> | Чтение/запись<br/> | Указывает, запустил ли пользователь клиентский элемент управления с помощью интерфейса Веб-доступ удаленных рабочих столов.<br/>                                                                                                  |
| [**маркрдпсеттингссекуре**](imsrdpclientnonscriptable4-markrdpsettingssecure.md)<br/>                     | Чтение/запись<br/> | Указывает, помечены ли параметры RDP как безопасные.<br/>                                                                                                                                          |
| [**промптфоркредсонклиент**](imsrdpclientnonscriptable4-promptforcredsonclient.md)<br/>                   | Чтение/запись<br/> | Указывает, отображает ли клиентский элемент управления диалоговое окно с запросом учетных данных.<br/>                                                                                                      |
| [**публишерцертификатечаин**](imsrdpclientnonscriptable4-publishercertificatechain.md)<br/>             | Чтение/запись<br/> | Указывает цепочку сертификатов издателя. Цепочка хранится в варианте типа VT \_ ByRef, который содержит указатель на структуру [**\_ \_ контекста цепочки сертификатов**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .<br/> |
| [**редиректионварнингтипе**](imsrdpclientnonscriptable4-redirectionwarningtype.md)<br/>                   | Чтение/запись<br/> | Управляет присутствием и внешним видом диалогового окна перенаправления.<br/>                                                                                                                           |
| [**трустедзонесите**](imsrdpclientnonscriptable4-trustedzonesite.md)<br/>                                 | Чтение/запись<br/> | Указывает, находится ли веб-сайт, с которого пользователь запустил подключение, в списке надежных сайтов клиентского компьютера.<br/>                                                                |
| [**варнабаутпринтерредиректион**](imsrdpclientnonscriptable4-warnaboutprinterredirection.md)<br/>         | Чтение/запись<br/> | Указывает, отображается ли в диалоговом окне перенаправление сообщение о перенаправлении принтера перед запуском сеанса.<br/>                                                                          |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | \_MSRDPCLIENT10 CLSID определен как C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> \_MSRDPCLIENT10NOTSAFEFORSCRIPTING CLSID определен как A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> \_MSRDPCLIENT6 CLSID определен как 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> \_MSRDPCLIENT6NOTSAFEFORSCRIPTING CLSID определен как D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> \_MSRDPCLIENT7 CLSID определен как A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> \_MSRDPCLIENT7NOTSAFEFORSCRIPTING CLSID определен как 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> \_MSRDPCLIENT8 CLSID определен как 5F681803-2900-4C43-A1CC-CF405404A676<br/> \_MSRDPCLIENT8NOTSAFEFORSCRIPTING CLSID определен как A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> \_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> \_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable4 определен как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**имсрдпклиентнонскриптабле**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**имстскнонскриптабле**](imstscnonscriptable-interface.md)
</dt> </dl>

 

