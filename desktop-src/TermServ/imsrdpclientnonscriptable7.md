---
title: Интерфейс IMsRdpClientNonScriptable7
description: Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable7
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable7, описание
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719222"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>Интерфейс IMsRdpClientNonScriptable7

Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) . Доступ к методам этого интерфейса возможен только через таблицу vtable; они недоступны для использования в сценариях клиентов.

Экземпляр этого интерфейса получен путем вызова [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для объекта [**имстскакс**](imstscax-interface.md) , передавая **IID \_ IMsRdpClientNonScriptable7**.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientNonScriptable7** наследует от [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable7** также имеет следующие типы членов:

- [Методы](#methods)
- [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **IMsRdpClientNonScriptable7** содержит следующие методы.


| Метод            | Описание              |
|:------------------|:-------------------------|
| [**дисабледпикурсорскалингфорпроцесс**](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  Отключает локальное масштабирование курсора мыши, полученного от сервера, обеспечивая правильную визуализацию формы курсора без изменения.                   |

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClientNonScriptable7** имеет следующие свойства.

| Свойство         | Тип доступа           | Описание            |
|:-----------------|:----------------------|:-----------------------|
| [**камераредирконфигколлектион**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | Только для чтения |  Возвращает коллекцию камер (и связанных конфигураций), доступных для перенаправления.   |
| [**Буфер обмена**](imsrdpclientnonscriptable7-clipboard.md)                       | Только для чтения |    Возвращает контроллер буфера обмена, используемый для синхронизации локальных и удаленных буферов обмена, если включена ручная синхронизация буфера обмена.    |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | \_MSRDPCLIENT12 CLSID определен как 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> \_MSRDPCLIENT12NOTSAFEFORSCRIPTING CLSID определен как 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> \_MSRDPCLIENT11 CLSID определен как 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> \_MSRDPCLIENT11NOTSAFEFORSCRIPTING CLSID определен как 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable7 определен как 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC            |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
