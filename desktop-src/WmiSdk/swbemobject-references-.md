---
description: Метод References \_ объекта SWbemObject Возвращает коллекцию всех классов ассоциации или экземпляров, ссылающихся на текущий объект.
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: Метод SWbemObject.References_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.References_
- ISWbemObject.References_
- ISWbemObject.References_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 527d49854f57937cfbcff8fd033381472f81cb15dc7ec1f4122a185fff33aa09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860214"
---
# <a name="swbemobjectreferences_-method"></a>SWbemObject. References, \_ метод

Метод **References \_** объекта [**SWbemObject**](swbemobject.md) Возвращает коллекцию всех классов ассоциации или экземпляров, ссылающихся на текущий объект.

Этот метод выполняет ту же функцию, что и [ссылки на](references-of-statement.md) WQL-запрос.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objWbemObjectSet = .References_( _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стрресулткласс* \[ в необязательное\]
</dt> <dd>

Строка, содержащая имя класса. Если этот параметр указан, он указывает, что возвращаемые объекты ассоциации должны принадлежать или быть производными от класса, указанного в этом параметре.

</dd> <dt>

*strRole* \[ в необязательное\]
</dt> <dd>

Строка, содержащая имя свойства. Если этот параметр задан, он указывает, что возвращаемые объекты связи должны быть ограничены теми, в которых исходный объект играет определенную роль. Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.

</dd> <dt>

*бклассесонли* \[ в необязательное\]
</dt> <dd>

Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов. Это классы, к которым принадлежат объекты взаимосвязей. Значение по умолчанию для этого параметра — **false**.

</dd> <dt>

*бсчемаонли* \[ в необязательное\]
</dt> <dd>

Логическое значение, указывающее, применяется ли запрос к схеме, а не к данным. Значение по умолчанию для этого параметра — **false**. Можно задать только **значение true** , если объект, для которого вызывается этот метод, является классом. Если задано **значение true**, набор возвращаемых конечных точек представляет классы, которые связаны с исходным классом в схеме.

</dd> <dt>

*стррекуиредкуалифиер* \[ в необязательное\]
</dt> <dd>

Строка, содержащая имя квалификатора. Если этот параметр указан, он указывает, что возвращаемые объекты связи должны включать указанный квалификатор.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Целое число, указывающее дополнительные флаги для операции. По умолчанию для этого параметра задано значение **вбемфлагретурниммедиатели**, которое направляет вызов для возврата немедленно, а не ожидания завершения запроса. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли * * * * (32 (0x20))


</dt> <dd>

Вызывает возврат перечислителя "только вперед". Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал * * * * (0 (0x0))


</dt> <dd>

заставляет инструментарий управления Windows (WMI) (WMI) хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели * * * * (16 (0x10))


</dt> <dd>

Приводит к немедленному возврату вызова.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете * * * * (0 (0x0))


</dt> <dd>

Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс * * * * (131072 (0x20000))


</dt> <dd>

Заставляет WMI возвращать данные о поправности класса с определением базового класса. Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если вызов выполнен успешно, возвращается объект [**SWbemObjectSet**](swbemobjectset.md) .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **References \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> </dl>

## <a name="remarks"></a>Remarks

Дополнительные сведения о ССЫЛКАх на связанный WQL-запрос, исходные экземпляры и объекты связи см. в разделе [соединители оператора](associators-of-statement.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject. соединители\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemServices. АссоЦиаторсоф**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices. Референцесто**](swbemservices-referencesto.md)
</dt> </dl>

 

 




