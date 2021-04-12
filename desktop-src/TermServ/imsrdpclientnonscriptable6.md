---
title: Интерфейс IMsRdpClientNonScriptable6
description: Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса IMsRdpClientNonScriptable5.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable6
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable6, описание
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104416361"
---
# <a name="imsrdpclientnonscriptable6-interface"></a>Интерфейс IMsRdpClientNonScriptable6

Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) . Доступ к методам этого интерфейса возможен только через таблицу vtable; они недоступны для использования в сценариях клиентов.

Экземпляр этого интерфейса получен путем вызова [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для объекта [**имстскакс**](imstscax-interface.md) , передавая **IID \_ IMsRdpClientNonScriptable6**.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientNonScriptable6** наследует от [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable6** также имеет следующие типы членов:

- [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IMsRdpClientNonScriptable6** содержит следующие методы.


| Метод            | Описание                   |
|:-----------------------------|:-----------------|
| [**SendLocation2D**](imsrdpclientnonscriptable6-sendlocation2d.md)     |  Отправляет на сервер значение широты и долготы, благодаря чему географическое расположение клиента может быть отражено в удаленном сеансе.                   |
| [**SendLocation3D**](imsrdpclientnonscriptable6-sendlocation3d.md)     | Отправляет на сервер значение широты, долготы и высоты, чтобы географическое расположение клиента можно было отражать в удаленном сеансе.                 |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1709 (сборка 16299)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | \_MSRDPCLIENT12 CLSID определен как 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> \_MSRDPCLIENT12NOTSAFEFORSCRIPTING CLSID определен как 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> \_MSRDPCLIENT11 CLSID определен как 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> \_MSRDPCLIENT11NOTSAFEFORSCRIPTING CLSID определен как 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable6 определен как 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>
