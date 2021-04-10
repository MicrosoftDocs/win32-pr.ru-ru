---
description: Метод Путасинк \_ объекта SWbemObject асинхронно создает или обновляет объект экземпляра или класса для Инструментарий управления Windows (WMI) (WMI).
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: Метод SWbemObject.PutAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272568"
---
# <a name="swbemobjectputasync_-method"></a>SWbemObject. Путасинк, \_ метод

Метод **путасинк \_** объекта [**SWbemObject**](swbemobject.md) асинхронно создает или обновляет объект экземпляра или класса для Инструментарий управления Windows (WMI) (WMI). Этот метод можно использовать после изменения любых свойств или методов в **SWbemObject**, и ваши изменения записываются в WMI.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемсинк* \[ окне\]
</dt> <dd>

Обязательный. Приемник объекта, который асинхронно получает результат операции **размещения** .

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Определяет, создает ли вызов или обновляет класс или экземпляр, и, если вызов возвращается немедленно. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>Вбемчанжефлагупдатекомпатибле * * * * (0 (0x0))


</dt> <dd>

Позволяет обновлять класс, если нет производных классов и для этого класса нет экземпляров. Это также позволяет обновлять во всех случаях, если изменение относится только к неважным квалификаторам (например, квалификатору **Description** ). Это поведение по умолчанию для этого вызова и используется для совместимости с предыдущими версиями инструментария WMI. Если в классе есть экземпляры, происходит сбой обновления.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>Вбемчанжефлагупдатесафемоде * * * * (32 (0x20))


</dt> <dd>

Позволяет обновлять классы даже при наличии дочерних классов, если изменение не вызывает конфликтов с дочерними классами. Этот флаг можно использовать при добавлении нового свойства в базовый класс, который ранее не упоминался ни в одном из дочерних классов. Если в классе есть экземпляры, происходит сбой обновления.

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>Вбемчанжефлагупдатефорцемоде * * * * (64 (0x40))


</dt> <dd>

Принудительно обновляет классы при наличии конфликтующих дочерних классов. Например, этот флаг приводит к принудительному обновлению, если квалификатор класса был определен в дочернем классе, а базовый класс пытается добавить тот же квалификатор в конфликт с существующим. В принудительном режиме этот конфликт разрешается путем удаления конфликтующего квалификатора в дочернем классе. Если в классе есть экземпляры, происходит сбой обновления.

Использование принудительного режима для обновления статического класса приводит к удалению всех экземпляров этого класса. Принудительное обновление класса поставщика не удаляет экземпляры класса.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>Вбемчанжефлагкреатеорупдате * * * * (0 (0x0))


</dt> <dd>

Вызывает создание класса или экземпляра, если он не существует или перезаписан, если он уже существует.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>Вбемчанжефлагкреатеонли * * * * (0x2)


</dt> <dd>

Используется только для создания. Вызов завершается ошибкой, если класс или экземпляр уже существует.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>Вбемчанжефлагупдатеонли * * * * (1 (0x1))


</dt> <dd>

Приводит к обновлению этого вызова. Для успешного вызова должен существовать класс или экземпляр.

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

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус * * * * (128 (0x80))


</dt> <dd>

Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**свбемсинк. OnProgress**](swbemsink-onprogress.md) для приемника объекта.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус * * * * (0 (0x0))


</dt> <dd>

Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс * * * * (131072 (0x20000))


</dt> <dd>

Заставляет Инструментарий WMI записывать данные о поправности классов вместе с определением базового класса. Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует эту информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> <dt>

*обжвбемасинкконтекст* \[ в необязательное\]
</dt> <dd>

Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова. Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта. Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов. Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) . Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение. Если вызов выполнен успешно, событие [**онобжектпут**](swbemsink-onobjectput.md) переданного приемника объекта получает объект [**свбемобжектпас**](swbemobjectpath.md) , содержащий путь к объекту экземпляра или класса, который успешно зафиксирован в WMI.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **путасинк \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

У текущего пользователя нет разрешения на обновление экземпляра указанного класса.

</dd> <dt>

**вбемерралреадексистс** -2147749913 (0x80041019)
</dt> <dd>

Был указан флаг **вбемчанжефлагкреатеонли** , но экземпляр уже существует.

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерриллегалнулл** -2147749898 (0x8004100A)
</dt> <dd>

Для свойства, которое не может быть **Nothing**, указано значение **Nothing** . Примером такого свойства является атрибут, помеченный квалификатором **Key**, **индексированного** или **Not \_ null** .

</dd> <dt>

**вбемерринвалидобжект** -2147749908 (0x80041014)
</dt> <dd>

Задан недопустимый экземпляр.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Был указан флаг **вбемчанжефлагупдатеонли** , но экземпляр или класс не существует.

</dd> <dt>

**вбемерринкомплетекласс** -2147749920 (0x80041020)
</dt> <dd>

Обязательные свойства для классов не заданы.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот вызов возвращает немедленно, и результат операции **размещения** возвращается вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*. Реализуйте *обжвбемсинк*. Метод [**онобжектпут**](swbemsink-onobjectput.md) для получения пути к объекту экземпляра или класса, который записывается в репозиторий WMI. Дополнительные сведения о методах приемника см. [в разделе вызов метода](calling-a-method.md).

Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник. Это создает угрозы безопасности для сценариев и приложений. Чтобы устранить риски, используйте семисинчронаус или синхронный обмен данными. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

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

[**Свбемобжектпас. класс**](swbemobjectpath-class.md)
</dt> <dt>

[**SWbemProperty**](swbemproperty.md)
</dt> <dt>

[**свбемкуалифиер**](swbemqualifier.md)
</dt> </dl>

 

