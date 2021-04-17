---
description: Предоставляет расширенные функциональные возможности для SWbemObject. Как и SWbemObject, методы этого расширенного объекта могут использоваться всеми объектами WMI.
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: Объект Свбемобжектекс (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: abed8c1d58687203aaeb32918cf15b2785b92622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711638"
---
# <a name="swbemobjectex-object"></a>Объект Свбемобжектекс

Объект **свбемобжектекс** предоставляет расширенные функциональные возможности для [**SWbemObject**](swbemobject.md). Как и **SWbemObject**, методы этого расширенного объекта могут использоваться всеми объектами WMI. Не удается создать этот объект с [помощью вызова функции](/previous-versions//xzysf6hc(v=vs.85)) VBScript.

## <a name="members"></a>Элементы

Объект **свбемобжектекс** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **свбемобжектекс** содержит эти методы.



| Метод                                      | Описание                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [**GetText\_**](swbemobjectex-gettext-.md) | Возвращает текстовый файл, показывающий содержимое объекта в формате XML.<br/> |
| [**Обновить\_**](swbemobjectex-refresh-.md) | Обновляет данные в объекте.<br/>                                  |
| **сетфромтекст\_**                           | Зарезервировано для последующего использования.<br/>                                      |



 

### <a name="properties"></a>Свойства

Объект **свбемобжектекс** имеет следующие свойства.



| Свойство                                                                 | Тип доступа           | Описание                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**системпропертиес\_**](swbemobjectex-systemproperties-.md)<br/> | Чтение/запись<br/> | Объект [**SWbemPropertySet**](swbempropertyset.md) , содержащий коллекцию системных свойств, которые применяются к **свбемобжектекс**.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМОБЖЕКТЕКС CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемобжектекс<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[вбемобжекттекстформатенум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

