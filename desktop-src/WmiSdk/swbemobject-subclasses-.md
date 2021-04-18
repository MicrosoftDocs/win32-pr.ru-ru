---
description: Метод подклассов \_ объекта SWbemObject возвращает объект SWbemObjectSet.
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: Метод SWbemObject.Subclasses_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692696"
---
# <a name="swbemobjectsubclasses_-method"></a>Метод SWbemObject. подклассов \_

Метод **подклассов \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**SWbemObjectSet**](swbemobjectset.md) . Этот объект представляет собой коллекцию подклассов текущего объекта, который должен быть классом. Элементы в возвращаемой коллекции можно получить с помощью стандартных методов сбора. Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Целое число, определяющее, как детально перечисляются вызовы. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>Вбемкуерифлагдип * * * * (0 (0x0))


</dt> <dd>

Активирует рекурсивное перечисление во всех подклассах, производных от указанного родительского класса. Сам родительский класс не возвращается в перечислении.

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>Вбемкуерифлагшаллов * * * * (1 (0x1))


</dt> <dd>

Значение по умолчанию для этого параметра. Он заставляет перечисление включать только непосредственные подклассы указанного родительского класса.

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели * * * * (16 (0x10))


</dt> <dd>

Приводит к немедленному возврату вызова

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете * * * * (0 (0x0))


</dt> <dd>

Вызывает блокирование этого вызова до завершения вызова.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс * * * * (131072 (0x20000))


</dt> <dd>

Заставляет Инструментарий WMI возвращать данные о поправности классов вместе с определением базового класса.

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если вызов выполнен успешно, возвращается объект [**SWbemObjectSet**](swbemobjectset.md) .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **подклассов \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидкласс** -2147749904 (0x80041010)
</dt> <dd>

Указанный класс не существует.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если в возвращаемой коллекции нет подклассов текущего объекта, то не будет возвращать нулевые элементы. Метод **подклассов \_** работает только для объектов класса.

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

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

 




