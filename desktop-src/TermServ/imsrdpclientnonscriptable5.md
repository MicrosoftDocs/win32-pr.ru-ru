---
title: Интерфейс IMsRdpClientNonScriptable5
description: предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса IMsRdpClientNonScriptable4.
ms.assetid: 41b8c624-0451-4a7e-bc80-d0bf269e33c6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, описание
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb7f3407f0dc6b1bc8dc04c6c4a72cda95db6b6b1def088a18908a730b96600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009804"
---
# <a name="imsrdpclientnonscriptable5-interface"></a>Интерфейс IMsRdpClientNonScriptable5

предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md) . Доступ к методам этого интерфейса возможен только через таблицу vtable; они недоступны для использования в сценариях клиентов.

Экземпляр этого интерфейса получен путем вызова [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для объекта [**имстскакс**](imstscax-interface.md) , передавая **IID \_ IMsRdpClientNonScriptable5**.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientNonScriptable5** наследует от [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md). **IMsRdpClientNonScriptable5** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **IMsRdpClientNonScriptable5** имеет следующие свойства.



| Свойство                                                                                                         | Тип доступа           | Описание                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**алловпромптингфоркредентиалс**](imsrdpclientnonscriptable5-allowpromptingforcredentials.md)<br/>       | Чтение/запись<br/> | указывает, может ли элемент управления ActiveX удаленный рабочий стол запрашивать учетные данные у пользователя.<br/>                    |
| [**дисаблеконнектионбар**](imsrdpclientnonscriptable5-disableconnectionbar.md)<br/>                       | Только на запись<br/> | указывает, должен ли элемент управления ActiveX удаленный рабочий стол отключить панель подключения.<br/>                      |
| [**дисаблеремотеаппкапсчекк**](imsrdpclientnonscriptable5-disableremoteappcapscheck.md)<br/>             | Чтение/запись<br/> | указывает, должен ли элемент управления ActiveX удаленный рабочий стол не проверять возможности RemoteApp на сервере.<br/> |
| [**жетремотемониторсбаундингбокс**](imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md)<br/>       | Только для чтения<br/>  | Задает ограничивающий прямоугольник удаленного монитора.<br/>                                                      |
| [**ремотемониторкаунт**](imsrdpclientnonscriptable5-remotemonitorcount.md)<br/>                           | Только для чтения<br/>  | Указывает число удаленных мониторов.<br/>                                                                     |
| [**ремотемониторлайаутматчеслокал**](imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md)<br/> | Только для чтения<br/>  | Указывает, идентичен ли макет удаленного монитора структуре локального монитора.<br/>                             |
| [**усемултимон**](imsrdpclientnonscriptable5-usemultimon.md)<br/>                                         | Чтение/запись<br/> | указывает, должен ли элемент управления ActiveX удаленный рабочий стол использовать несколько мониторов.<br/>                           |
| [**варнабаутдиректксредиректион**](imsrdpclientnonscriptable5-warnaboutdirectxredirection.md)<br/>         | Чтение/запись<br/> | Это свойство не используется.<br/>                                                                                   |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | \_MSRDPCLIENT10 CLSID определен как C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> \_MSRDPCLIENT10NOTSAFEFORSCRIPTING CLSID определен как A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> \_MSRDPCLIENT7 CLSID определен как A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> \_MSRDPCLIENT7NOTSAFEFORSCRIPTING CLSID определен как 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> \_MSRDPCLIENT8 CLSID определен как 5F681803-2900-4C43-A1CC-CF405404A676<br/> \_MSRDPCLIENT8NOTSAFEFORSCRIPTING CLSID определен как A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> \_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> \_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

