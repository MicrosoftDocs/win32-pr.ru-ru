---
description: Объект SWbemPropertySet — это коллекция объектов SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Объект SWbemPropertySet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712929"
---
# <a name="swbempropertyset-object"></a>Объект SWbemPropertySet

Объект **SWbemPropertySet** — это коллекция объектов [**SWbemProperty**](swbemproperty.md) . Вы можете добавлять элементы в коллекцию с помощью метода [**Add**](swbempropertyset-add.md) , получать элементы из коллекции с помощью метода [**Item**](swbempropertyset-item.md) и удалять элементы из коллекции с помощью метода [**Remove**](swbempropertyset-remove.md) . Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md). Не удается создать этот объект с [помощью вызова функции](creating-an-object-using-vbscript.md) VBScript.

Объекты [**SWbemProperty**](swbemproperty.md) , составляющие коллекцию **SWbemPropertySet** , используются для описания свойств одного класса или экземпляра WMI.

## <a name="members"></a>Элементы

Объект **SWbemPropertySet** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **SWbemPropertySet** содержит эти методы.



| Метод                                    | Описание                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Включить**](swbempropertyset-add.md)       | Добавляет объект [**SWbemProperty**](swbemproperty.md) в коллекцию **SWbemPropertySet** .<br/>                        |
| [**Элемент**](swbempropertyset-item.md)     | Возвращает именованный [**SWbemProperty**](swbemproperty.md) из коллекции. Это метод по умолчанию для этого объекта.<br/> |
| [**Отменит**](swbempropertyset-remove.md) | Удаляет объект [**SWbemProperty**](swbemproperty.md) из коллекции.<br/>                                        |



 

### <a name="properties"></a>Свойства

Объект **SWbemPropertySet** имеет следующие свойства.



| Свойство                                           | Тип доступа          | Описание                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [**Расчета**](swbempropertyset-count.md)<br/> | Только для чтения<br/> | Число элементов в коллекции **SWbemPropertySet** .<br/> |



 

## <a name="examples"></a>Примеры

В следующем примере VBScript показано, как [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) может возвращать **вбемеррресеттодефаулт** , если свойство переопределено.


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTYSET CLSID<br/>                                                      |
| IID<br/>                      | IID \_ исвбемпропертисет<br/>                                                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




