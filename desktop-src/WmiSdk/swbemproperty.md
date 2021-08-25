---
description: Объект SWbemProperty представляет отдельное свойство WMI управляемого объекта. Не удается создать этот объект с помощью вызова функции VBScript.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Объект SWbemProperty (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 51f4b1b22849fc5a6ae22f49c5c30411563efb9d133cf2440c301eabfde18e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898074"
---
# <a name="swbemproperty-object"></a>Объект SWbemProperty

Объект **SWbemProperty** представляет отдельное свойство WMI управляемого объекта. Не удается создать этот объект с [помощью вызова функции](creating-an-object-using-vbscript.md) VBScript.

## <a name="members"></a>Элементы

Объект **SWbemProperty** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Объект **SWbemProperty** имеет следующие свойства.



| Свойство                                                     | Тип доступа           | Описание                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**Цимтипе**](swbemproperty-cimtype.md)<br/>          | Только для чтения<br/>  | Тип этого свойства.<br/>                                                                                             |
| [**IsArray**](swbemproperty-isarray.md)<br/>          | Только для чтения<br/>  | Логическое значение, указывающее, имеет ли это свойство тип массива.<br/>                                                   |
| [**Локальный**](swbemproperty-islocal.md)<br/>          | Только для чтения<br/>  | Логическое значение, указывающее, является ли это свойство локальным.<br/>                                                            |
| [**Имя**](swbemproperty-name.md)<br/>                | Только для чтения<br/>  | Имя этого свойства WMI.<br/>                                                                                         |
| [**Исходный домен**](swbemproperty-origin.md)<br/>            | Только для чтения<br/>  | Содержит исходный класс этого свойства.<br/>                                                                   |
| [**Квалификаторы\_**](swbemproperty-qualifiers-.md)<br/> | Только для чтения<br/>  | Объект [**свбемкуалифиерсет**](swbemqualifierset.md) , являющийся коллекцией квалификаторов для этого свойства.<br/> |
| [**Значение**](swbemproperty-value.md)<br/>              | Чтение/запись<br/> | Фактическое значение этого свойства. Это свойство автоматизации данного объекта по умолчанию.<br/>                             |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемпроперти<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




