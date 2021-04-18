---
description: Интерфейс Ипортабледевицевалуес содержит коллекцию пар PROPERTYKEY/ПРОПВАРИАНТ.
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: Интерфейс Ипортабледевицевалуес (Портабледевицетипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ecdfd91c9ea4ab5202a72015f579d560b37fbffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694474"
---
# <a name="iportabledevicevalues-interface"></a>Интерфейс Ипортабледевицевалуес

Интерфейс **ипортабледевицевалуес** содержит коллекцию пар **PROPERTYKEY** / **пропвариант** . Значения в коллекции не обязательно должны совпадать с теми же VARTYPE.

Значения хранятся в виде пар "ключ-значение". Каждый ключ должен быть уникальным в коллекции. Клиенты могут искать элементы по **PROPERTYKEY** или индексу, начинающимся с нуля. Значения данных хранятся в виде структур **пропвариант** . Можно добавлять или извлекать значения любого типа с помощью универсальных методов **SetValue** и **GetValue**, а также добавлять элементы с помощью метода, относящегося к типу добавляемых данных.

Для методов **Get...** требуется, чтобы вызывающий объект освободил все извлеченные значения соответствующим образом. Методы **Set...** копируют значение в коллекцию.

При освобождении интерфейса **ипортабледевицевалуес** вызывается метод **clear**, который освобождает память, выделенную для всех его элементов соответствующим образом.

Этот интерфейс можно получить из метода или, если требуется новый объект, вызовите **CREATE** с помощью **CLSID \_ портабледевицевалуес**.

## <a name="members"></a>Элементы

Интерфейс **ипортабледевицевалуес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ипортабледевицевалуес** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ипортабледевицевалуес** содержит следующие методы.



| Метод                                                                                                                     | Описание                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Открытым**](iportabledevicevalues-clear.md)                                                                               | Удаляет все элементы из коллекции.<br/>                                                                      |
| [**копивалуесфромпропертисторе**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | Копирует содержимое объекта **ипропертисторе** в коллекцию.<br/>                                           |
| [**копивалуестопропертисторе**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | Копирует все значения из коллекции в интерфейс **ипропертисторе** .<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | Извлекает значение из коллекции, используя указанный индекс, начинающийся с нуля.<br/>                                  |
| [**жетбулвалуе**](iportabledevicevalues-getboolvalue.md)                                                                 | Извлекает **логическое** значение (тип VT \_ bool), заданное ключом.<br/>                                              |
| [**жетбуффервалуе**](iportabledevicevalues-getbuffervalue.md)                                                             | Извлекает значение массива байтов (тип VT \_ vector \| VT \_ UI1), заданный ключом.<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | Возвращает количество элементов в коллекции.<br/>                                                            |
| [**жетеррорвалуе**](iportabledevicevalues-geterrorvalue.md)                                                               | Получает значение **HRESULT** (тип ошибки VT \_ ), заданное ключом.<br/>                                         |
| [**жетфлоатвалуе**](iportabledevicevalues-getfloatvalue.md)                                                               | Извлекает значение **float** (тип VT \_ R4), заданное ключом.<br/>                                               |
| [**жетгуидвалуе**](iportabledevicevalues-getguidvalue.md)                                                                 | Возвращает значение **GUID** (тип VT \_ CLSID), заданное ключом.<br/>                                             |
| [**жетипортабледевицекэйколлектионвалуе**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | Возвращает значение **ипортабледевицекэйколлектион** (тип VT \_ Unknown), заданное ключом.<br/>                  |
| [**жетипортабледевицепропвариантколлектионвалуе**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | Возвращает значение **ипортабледевицепропвариантколлектион** (тип VT \_ Unknown), заданное ключом.<br/>          |
| [**жетипортабледевицевалуесколлектионвалуе**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | Возвращает значение **ипортабледевицевалуесколлектион** (тип VT \_ Unknown), заданное ключом.<br/>               |
| [**жетипортабледевицевалуесвалуе**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | Возвращает значение **ипортабледевицевалуес** (тип VT \_ Unknown), заданное ключом.<br/>                         |
| [**жетиункновнвалуе**](iportabledevicevalues-getiunknownvalue.md)                                                         | Извлекает значение интерфейса **IUnknown** (тип VT \_ Unknown), заданное ключом.<br/>                            |
| [**жеткэйвалуе**](iportabledevicevalues-getkeyvalue.md)                                                                   | Извлекает значение **PROPERTYKEY** , заданное ключом.<br/>                                                       |
| [**жетсигнединтежервалуе**](iportabledevicevalues-getsignedintegervalue.md)                                               | Извлекает **длинное** значение (тип VT \_ i4), заданное ключом.<br/>                                                |
| [**жетсигнедларжеинтежервалуе**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | Извлекает значение **лонглонг** (Type VT \_ I8), заданное ключом.<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | Извлекает строковое значение (тип VT \_ LPWSTR), заданное ключом.<br/>                                              |
| [**жетунсигнединтежервалуе**](iportabledevicevalues-getunsignedintegervalue.md)                                           | Извлекает значение типа **ulong** (тип VT \_ UI4), заданное ключом.<br/>                                              |
| [**жетунсигнедларжеинтежервалуе**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | Извлекает значение **улонглонг** (Type VT \_ UI8), заданное ключом.<br/>                                          |
| [**GetValue**](iportabledevicevalues-getvalue.md)                                                                         | Извлекает значение **пропвариант** , заданное ключом.<br/>                                                       |
| [**ремовевалуе**](iportabledevicevalues-removevalue.md)                                                                   | Удаляет элемент из коллекции.<br/>                                                                        |
| [**SetBoolValue**](iportabledevicevalues-setboolvalue.md)                                                                 | Добавляет новое **логическое** значение (тип VT \_ bool) или перезаписывает существующий.<br/>                                 |
| [**сетбуффервалуе**](iportabledevicevalues-setbuffervalue.md)                                                             | Добавляет новое значение **байта** \* (тип VT \_ vector \| VT \_ UI1) или перезаписывает существующий.<br/>                     |
| [**сетеррорвалуе**](iportabledevicevalues-seterrorvalue.md)                                                               | Добавляет новое значение **HRESULT** (тип ошибки VT \_ ) или перезаписывает существующую.<br/>                                |
| [**сетфлоатвалуе**](iportabledevicevalues-setfloatvalue.md)                                                               | Добавляет новое значение **float** (Type VT \_ R4) или перезаписывает существующий.<br/>                                     |
| [**сетгуидвалуе**](iportabledevicevalues-setguidvalue.md)                                                                 | Добавляет новое значение **GUID** (тип VT \_ CLSID) или перезаписывает существующий.<br/>                                   |
| [**сетипортабледевицекэйколлектионвалуе**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | Добавляет новое значение **ипортабледевицекэйколлектионвалуе** (тип VT \_ Unknown) или перезаписывает существующий.<br/>    |
| [**сетипортабледевицепропвариантколлектионвалуе**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | Добавляет новое значение **ипортабледевицепропвариантколлектион** (тип VT \_ Unknown) или перезаписывает существующий.<br/> |
| [**сетипортабледевицевалуесколлектионвалуе**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | Добавляет новое значение **ипортабледевицевалуесколлектион** (тип VT \_ Unknown) или перезаписывает существующий.<br/>      |
| [**сетипортабледевицевалуесвалуе**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | Добавляет новое значение **ипортабледевицевалуес** (тип VT \_ Unknown) или перезаписывает существующий.<br/>                |
| [**сетиункновнвалуе**](iportabledevicevalues-setiunknownvalue.md)                                                         | Добавляет новое значение **IUnknown** (тип VT \_ Unknown) или перезаписывает существующий.<br/>                             |
| [**сеткэйвалуе**](iportabledevicevalues-setkeyvalue.md)                                                                   | Добавляет новое значение **PROPERTYKEY** (типа VT \_ Unknown) или перезаписывает существующий.<br/>                          |
| [**сетсигнединтежервалуе**](iportabledevicevalues-setsignedintegervalue.md)                                               | Добавляет новое **длинное** значение (тип VT \_ i4) или перезаписывает существующий.<br/>                                      |
| [**сетсигнедларжеинтежервалуе**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | Добавляет новое значение **лонглонг** (Type VT \_ I8) или перезаписывает существующий.<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | Добавляет новое строковое значение (тип VT \_ LPWSTR) или перезаписывает существующий.<br/>                                    |
| [**сетунсигнединтежервалуе**](iportabledevicevalues-setunsignedintegervalue.md)                                           | Добавляет новое значение типа **ulong** (тип VT \_ UI4) или перезаписывает существующий.<br/>                                    |
| [**сетунсигнедларжеинтежервалуе**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | Добавляет новое значение **улонглонг** (Type VT \_ UI8) или перезаписывает существующий.<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | Добавляет новое значение **пропвариант** или перезаписывает существующий.<br/>                                             |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейсы коллекции**](collection-interfaces.md)
</dt> </dl>

 

