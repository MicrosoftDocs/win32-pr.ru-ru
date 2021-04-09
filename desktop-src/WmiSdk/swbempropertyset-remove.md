---
description: Метод Remove объекта SWbemPropertySet Удаляет свойство из коллекции SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: Метод SWbemPropertySet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155826"
---
# <a name="swbempropertysetremove-method"></a>SWbemPropertySet. Remove, метод

Метод **Remove** объекта [**SWbemPropertySet**](swbempropertyset.md) Удаляет свойство из коллекции **SWbemPropertySet** .

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*strName* \[ окне\]
</dt> <dd>

Обязательный. Имя удаляемого элемента.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано. Если указано, это значение должно быть равно 0 (нулю).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Remove** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Неопределенный сбой.

</dd> <dt>

**вбемерринвалидоператион** -2147749910 (0x80041016)
</dt> <dd>

Пользователь попытался удалить свойство, которое не может быть удалено.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Указанное свойство не существует.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для выполнения этого метода.

</dd> <dt>

**вбемеррпропагатедпроперти** -142927303552 (0x2147219380)
</dt> <dd>

Пользователь попытался удалить свойство, владельцем которого он не является. Свойство было унаследовано от класса-родителя.

</dd> <dt>

**вбемеррресеттодефаулт** -2147758082 (0x80043002)
</dt> <dd>

Пользователь удалил значение переопределения по умолчанию для текущего класса. Значение по умолчанию для этого свойства в родительском классе было повторно активировано.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Невозможно удалить свойства из экземпляров класса или производных классов с унаследованными свойствами. Такие попытки удаления вызывают ошибку, и свойство не удаляется. свойство сбрасывается до значения по умолчанию.

Невозможно выполнить итерацию коллекции при удалении элементов, так как при удалении элемента из коллекции указатель коллекции перемещается к следующему элементу. Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).

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

[**SWbemPropertySet. Add**](swbempropertyset-add.md)
</dt> </dl>

 

 




