---
description: Метод Instances \_ объекта SWbemObject создает перечислитель, который возвращает экземпляры текущего объекта класса. Этот метод реализует простой запрос. Более сложные запросы могут потребовать использования SWbemServices.ExeКкуери.
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.tgt_platform: multiple
title: Метод SWbemObject.Instances_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Instances_
- ISWbemObject.Instances_
- ISWbemObject.Instances_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c573c1e94cd473d22483c7b6a2c801c3e6bcb9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712896"
---
# <a name="swbemobjectinstances_-method"></a>SWbemObject. Instances, \_ метод

Метод **Instances \_** объекта [**SWbemObject**](swbemobject.md) создает перечислитель, который возвращает экземпляры текущего объекта класса. Этот метод реализует простой запрос. Более сложные запросы могут потребовать использования [**SWbemServices.Exeккуери**](swbemservices-execquery.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objWbemObjectSet = .Instances_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Целое число, определяющее поведение вызова. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли * * * * (32 (0x20))


</dt> <dd>

Вызывает возврат перечислителя "только вперед". Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал * * * * (0 (0x0))


</dt> <dd>

Заставляет Инструментарий WMI хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели * * * * (16 (0x10))


</dt> <dd>

Значение по умолчанию для этого параметра. Этот флаг приводит к немедленному возврату вызова.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете * * * * (0 (0x0))


</dt> <dd>

Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>Вбемкуерифлагшаллов * * * * (1 (0x1))


</dt> <dd>

Заставляет перечисление включать только непосредственные подклассы указанного родительского класса.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>Вбемкуерифлагдип * * * * (0 (0x0))


</dt> <dd>

Значение по умолчанию для этого параметра. Это значение приводит к включению в перечисление всех классов в иерархии.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс * * * * (131072 (0x20000))


</dt> <dd>

Заставляет WMI возвращать данные о поправности класса с определением базового класса.

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, объект [**SWbemObjectSet**](swbemobjectset.md) возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Instances \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

У текущего пользователя нет разрешения на просмотр экземпляров указанного класса.

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Произошла неопределенная ошибка.

</dd> <dt>

**вбемерринвалидкласс** -2147749904 (0x80041010)
</dt> <dd>

Указан недопустимый класс.

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

Метод **Instances \_** работает только для объектов класса. Возвращаемая коллекция не содержит нулевых элементов. Поведение по умолчанию для этого метода — [*семисинчронаус*](gloss-s.md) из-за значения *ифлагс* по умолчанию **вбемфлагретурниммедиатели**.

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

 

 




