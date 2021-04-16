---
description: Метод Add объекта SWbemPropertySet добавляет объект SWbemProperty в коллекцию SWbemPropertySet. Если свойство с таким именем уже существует в коллекции, его содержимое заменяется новым определением.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Метод SWbemPropertySet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712895"
---
# <a name="swbempropertysetadd-method"></a>SWbemPropertySet. Add, метод

Метод **Add** объекта [**SWbemPropertySet**](swbempropertyset.md) добавляет объект [**SWbemProperty**](swbemproperty.md) в коллекцию **SWbemPropertySet** . Если свойство с таким именем уже существует в коллекции, его содержимое заменяется новым определением.

> [!Note]  
> После этой операции значение добавленного свойства равно **null** (не назначено). Чтобы задать или изменить значение свойства WMI, необходимо задать свойство [**value**](swbemdatetime-value.md) возвращаемого объекта [**SWbemProperty**](swbemproperty.md) .

 

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*strName* \[ окне\]
</dt> <dd>

Обязательный. Имя нового свойства.

</dd> <dt>

*иЦимтипе* \[ окне\]
</dt> <dd>

Обязательный. Целое число, представляющее квалификатор **Цимтипе** нового свойства. См. [**вбемЦимтипинум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) для списка с квалификаторами **Цимтипе** и их значениями.

</dd> <dt>

*бисаррай* \[ в необязательное\]
</dt> <dd>

Указывает, является ли свойство типом массива. Значение по умолчанию для этого параметра — **false**.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано и должно быть равно нулю, если указано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха этот метод возвращает объект [**SWbemProperty**](swbemproperty.md) , представляющий новое свойство. В противном случае возвращается **пустой** объект.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Add** объект **Err** может содержать один из кодов ошибок, приведенных ниже.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Неопределенный сбой.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для выполнения этого метода.

</dd> <dt>

**вбемерринвалидпропертитипе** -2147749930
</dt> <dd>

Квалификатор **Цимтипе** не распознан.

</dd> </dl>

## <a name="examples"></a>Примеры

Пример кода, в котором используется этот метод, см. в разделе [**SWbemPropertySet**](swbempropertyset.md) .

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

[**SWbemPropertySet**](swbempropertyset.md)
</dt> <dt>

[**SWbemPropertySet. Remove**](swbempropertyset-remove.md)
</dt> <dt>

[**SWbemProperty. Value**](swbemproperty-value.md)
</dt> </dl>

 

 




