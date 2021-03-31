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
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272746"
---
# <a name="swbemproperty-object"></a>Объект SWbemProperty

Объект **SWbemProperty** представляет отдельное свойство WMI управляемого объекта. Не удается создать этот объект с [помощью вызова функции](creating-an-object-using-vbscript.md) VBScript.

## <a name="members"></a>Элементы

Объект **SWbemProperty** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **SWbemProperty** имеет следующие свойства.



| Свойство                                                     | Тип доступа           | Описание                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**Цимтипе**](swbemproperty-cimtype.md)<br/>          | Только для чтения<br/>  | Тип этого свойства.<br/>                                                                                             |
| [**IsArray**](swbemproperty-isarray.md)<br/>          | Только для чтения<br/>  | Логическое значение, указывающее, имеет ли это свойство тип массива.<br/>                                                   |
| [**Локальный**](swbemproperty-islocal.md)<br/>          | Только для чтения<br/>  | Логическое значение, указывающее, является ли это свойство локальным.<br/>                                                            |
| [**Имя**](swbemproperty-name.md)<br/>                | Только для чтения<br/>  | Имя этого свойства WMI.<br/>                                                                                         |
| [**Лета**](swbemproperty-origin.md)<br/>            | Только для чтения<br/>  | Содержит исходный класс этого свойства.<br/>                                                                   |
| [**Квалификаторы\_**](swbemproperty-qualifiers-.md)<br/> | Только для чтения<br/>  | Объект [**свбемкуалифиерсет**](swbemqualifierset.md) , являющийся коллекцией квалификаторов для этого свойства.<br/> |
| [**Значение**](swbemproperty-value.md)<br/>              | Чтение/запись<br/> | Фактическое значение этого свойства. Это свойство автоматизации данного объекта по умолчанию.<br/>                             |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемпроперти<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




