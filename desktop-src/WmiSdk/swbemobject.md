---
description: Методы и свойства объекта SWbemObject можно использовать для представления одного определения класса инструментарий управления Windows (WMI) (WMI) или экземпляра объекта.
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Объект SWbemObject (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701955"
---
# <a name="swbemobject-object"></a>Объект SWbemObject

Методы и свойства объекта **SWbemObject** можно использовать для представления одного определения класса инструментарий управления Windows (WMI) (WMI) или экземпляра объекта. Не удается создать этот объект с [помощью вызова функции](/previous-versions//xzysf6hc(v=vs.85)) VBScript.

Этот объект поддерживает два типа свойств и методов. Те, которые определены в этом разделе, являются универсальными свойствами и методами, применяемыми ко всем объектам WMI. Кроме того, этот объект предоставляет свойства и методы базового объекта в виде динамических свойств автоматизации и методов **SWbemObject**. Имена и типы этих свойств и методов зависят от базового объекта WMI. Дополнительные сведения о том, как предоставляются эти динамические свойства и методы, см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).

С точки зрения клиента WMI этот объект всегда находится внутри процесса. Операции записи затрагивают только локальную копию объекта, а операции чтения всегда извлекают значения из локальной копии. Обновления WMI выполняются только при написании целых объектов с помощью вызова метода [**SWbemObject. постановки \_**](swbemobject-put-.md) . При изменении свойств или методов в объекте **SWbemObject** изменения не записываются в WMI, пока не будет вызван метод **SWbemObject \_ .** WHERE.

Универсальный метод и имена свойств, определенные в этом разделе, всегда заканчиваются завершающим символом подчеркивания (" \_ "), чтобы отличать их от динамических методов и свойств WMI базового объекта.

Обратите внимание, что **SWbemObject** не может быть создано с помощью VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). Method. Если вы хотите создать новый пустой класс, используйте [**SwbemServices. Get**](swbemservices-get.md) с пустым параметром пути. Этот вызов возвращает пустой объект **SWbemObject** , который может стать классом. Затем можно указать имя класса для свойства [**класса**](swbemobjectpath-class.md) объекта [**свбемобжектпас**](swbemobjectpath.md) , возвращаемого вызовом [**path \_**](swbemobject-path-.md) . Добавьте свойства в новый класс с помощью метода [**Properties \_**](swbemobject-properties-.md) . Чтобы создать экземпляр, вызовите **GetObject** для нового класса.

В следующем примере кода показано, как получить новый класс и добавить в него свойство. Объект **SWbemObject** , представляющий класс, должен быть записан обратно в репозиторий WMI с помощью вызова метода " [**поставить \_**](swbemobject-put-.md)".


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



Вы можете проверить репозиторий с помощью средства просмотра, такого как [CIM Studio](further-information.md) , чтобы убедиться, что появился новый класс и экземпляр. Пример удаления класса и экземпляра из репозитория см. в разделе [**SwbemServices. Delete**](swbemservices-delete.md) или [**\_ SWbemObject. Delete**](swbemobject-delete-.md).

## <a name="members"></a>Элементы

Объект **SWbemObject** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **SWbemObject** содержит эти методы.



| Метод                                                        | Описание                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ASSOCIATORS\_**](swbemobject-associators-.md)             | Получает соединители объекта.<br/>                                                     |
| [**ассоЦиаторсасинк\_**](swbemobject-associatorsasync-.md)   | Асинхронно извлекает соединители объекта.<br/>                                      |
| [**Клонировать\_**](swbemobject-clone-.md)                         | Создает копию текущего объекта.<br/>                                                          |
| [**CompareTo\_**](swbemobject-compareto-.md)                 | Проверяет два объекта на равенство.<br/>                                                              |
| [**Удалить\_**](swbemobject-delete-.md)                       | Удаляет объект из WMI.<br/>                                                                 |
| [**DeleteAsync\_**](swbemobject-deleteasync-.md)             | Асинхронно удаляет объект из WMI.<br/>                                                  |
| [**ExecMethod\_**](swbemobject-execmethod-.md)               | Выполняет метод, экспортированный поставщиком метода.<br/>                                             |
| [**ексекмесодасинк\_**](swbemobject-execmethodasync-.md)     | Асинхронно выполняет метод, экспортированный поставщиком метода.<br/>                              |
| [**жетобжекттекст\_**](swbemobject-getobjecttext-.md)         | Извлекает текстовое представление объекта (синтаксис MOF).<br/>                             |
| [**Экземпляры\_**](swbemobject-instances-.md)                 | Возвращает коллекцию экземпляров объекта (который должен быть классом WMI).<br/>                 |
| [**инстанцесасинк\_**](swbemobject-instancesasync-.md)       | Асинхронно возвращает коллекцию экземпляров объекта (который должен быть классом WMI).<br/>  |
| [**PUT\_**](swbemobject-put-.md)                             | Создает или обновляет объект в WMI.<br/>                                                        |
| [**путасинк\_**](swbemobject-putasync-.md)                   | Асинхронно создает или обновляет объект в WMI.<br/>                                         |
| [**Ссылки\_**](swbemobject-references-.md)               | Возвращает ссылки на объект.<br/>                                                            |
| [**референцесасинк\_**](swbemobject-referencesasync-.md)     | Асинхронно возвращает ссылки на объект.<br/>                                             |
| [**SpawnDerivedClass\_**](swbemobject-spawnderivedclass-.md) | Создает новый производный класс из текущего объекта (который должен быть классом WMI).<br/>             |
| [**SpawnInstance\_**](swbemobject-spawninstance-.md)         | Создает новый экземпляр из текущего объекта.<br/>                                              |
| [**Подклассы\_**](swbemobject-subclasses-.md)               | Возвращает коллекцию подклассов объекта (который должен быть классом WMI).<br/>                |
| [**субклассесасинк\_**](swbemobject-subclassesasync-.md)     | Асинхронно возвращает коллекцию подклассов объекта (который должен быть классом WMI).<br/> |



 

### <a name="properties"></a>Свойства

Объект **SWbemObject** имеет следующие свойства.



| Свойство                                                   | Тип доступа          | Описание                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Наследование\_**](swbemobject-derivation-.md)<br/> | Только для чтения<br/> | Содержит массив строк, описывающих производную иерархию для класса.<br/>                                             |
| [**Методы\_**](swbemobject-methods-.md)<br/>       | Только для чтения<br/> | Объект [**свбеммесодсет**](swbemmethodset.md) , являющийся коллекцией методов для данного объекта.<br/>                           |
| [**Путь\_**](swbemobject-path-.md)<br/>             | Только для чтения<br/> | Содержит объект [**свбемобжектпас**](swbemobjectpath.md) , представляющий путь к объекту текущего класса или экземпляра.<br/> |
| [**Свойства\_**](swbemobject-properties-.md)<br/> | Только для чтения<br/> | Объект [**SWbemPropertySet**](swbempropertyset.md) , являющийся коллекцией свойств для данного объекта.<br/>                    |
| [**Квалификаторы\_**](swbemobject-qualifiers-.md)<br/> | Только для чтения<br/> | Объект [**свбемкуалифиерсет**](swbemqualifierset.md) , являющийся коллекцией квалификаторов для данного объекта.<br/>                  |
| [**Безопасность\_**](swbemobject-security-.md)<br/>     | Только для чтения<br/> | Содержит объект [**свбемсекурити**](swbemsecurity.md) , используемый для чтения или изменения параметров безопасности.<br/>                         |



 

## <a name="examples"></a>Примеры

[Список всех свойств и методов для](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) примера кода VBScript класса WMI в коллекции TechNet использует SWbemObject для перечисления всех методов и свойств для УКАЗАННОГО класса WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемобжектекс**](swbemobjectex.md)
</dt> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

