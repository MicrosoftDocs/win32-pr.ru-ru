---
description: Возвращает коллекцию всех классов или экземпляров взаимосвязей, которые ссылаются на конкретный исходный класс или экземпляр.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: SWbemServices. Референцесто, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73addea189815d1594d0963fbdd6e20c562b3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156759"
---
# <a name="swbemservicesreferencesto-method"></a>SWbemServices. Референцесто, метод

Метод **референцесто** объекта [**SwbemServices**](swbemservices.md) Возвращает коллекцию всех классов ассоциации или экземпляров, ссылающихся на конкретный исходный класс или экземпляр. Этот метод выполняет ту же функцию, что и [ссылки на](references-of-statement.md) WQL-запросы.

Этот метод вызывается в режиме семисинчронаус. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стробжектпас* 
</dt> <dd>

Обязательный. Строка, содержащая путь к объекту источника для этого метода. Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*стрресулткласс* \[ используемых\]
</dt> <dd>

Строка, содержащая имя класса. Если этот параметр указан, то возвращаемые объекты ассоциации должны принадлежать классу, указанному в этом параметре, или быть производным от него.

</dd> <dt>

*strRole* \[ используемых\]
</dt> <dd>

Строка, содержащая имя свойства. Если этот параметр задан, он указывает, что возвращаемые объекты связи должны быть ограничены теми, в которых исходный объект играет определенную роль. Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.

</dd> <dt>

*бклассесонли* \[ используемых\]
</dt> <dd>

Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов. Это классы, к которым принадлежат объекты взаимосвязей. Значение по умолчанию для этого параметра — **false**.

</dd> <dt>

*бсчемаонли* \[ используемых\]
</dt> <dd>

Логическое значение, указывающее, применяется ли запрос к схеме, а не к данным. Значение по умолчанию для этого параметра — **false**. Можно задать только **значение true** , если параметр *стробжектпас* указывает путь к объекту класса. Если задано **значение true**, набор возвращаемых конечных точек представляет классы, которые связаны с исходным классом в схеме.

</dd> <dt>

*стррекуиредкуалифиер* \[ используемых\]
</dt> <dd>

Строка, содержащая имя квалификатора. Если этот параметр указан, он указывает, что возвращаемые объекты связи должны включать указанный квалификатор.

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Целое число, задающее дополнительные флаги для операции. По умолчанию для этого параметра задано значение **вбемфлагретурниммедиатели**, которое направляет вызов для возврата немедленно, а не ожидания завершения запроса. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли * * * * (32 (0x20))


</dt> <dd>

Вызывает возврат перечислителя "только вперед". Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал * * * * (0 (0x0))


</dt> <dd>

Заставляет инструментарий управления Windows (WMI) (WMI) хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели * * * * (16 (0x10))


</dt> <dd>

Приводит к немедленному возврату вызова.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете * * * * (0 (0x0))


</dt> <dd>

Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен. Этот флаг вызывает метод в синхронном режиме.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс * * * * (131072 (0x20000))


</dt> <dd>

Заставляет Инструментарий WMI возвращать данные о поправности классов вместе с определением базового класса. Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, метод возвращает объект [**SWbemObjectSet**](swbemobjectset.md) .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **референцесто** объект **Err** может содержать один из кодов ошибок из следующего списка.

> [!Note]  
> Возвращенная коллекция с нулевым числом элементов не является ошибкой.

 

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

</dd> <dt>

**вбемфлагусеамендедкуалифиерс** -131072 (0x20000)
</dt> <dd>

Заставляет WMI возвращать данные о поправности класса с определением базового класса.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Дополнительные сведения о ССЫЛКАх на связанный WQL-запрос, исходные экземпляры и объекты связи см. в разделе [соединители оператора](associators-of-statement.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемсервицес<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject. соединители\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject. References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. АссоЦиаторсоф**](swbemservices-associatorsof.md)
</dt> </dl>

 

 




