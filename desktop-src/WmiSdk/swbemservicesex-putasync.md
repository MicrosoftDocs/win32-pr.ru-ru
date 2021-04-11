---
description: Асинхронно сохраняет объект в пространстве имен. При успешном выполнении этот метод отправляет oncompleteное событие в объект Свбемсинк, указанный в качестве входного параметра.
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.tgt_platform: multiple
title: Свбемсервицесекс. Путасинк, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 06f470ed6f8cbd497ba3d3a3a77c5a8b4e5748c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081112"
---
# <a name="swbemservicesexputasync-method"></a>Свбемсервицесекс. Путасинк, метод

Метод **путасинк** объекта [**свбемсервицесекс**](swbemservicesex.md) асинхронно сохраняет объект в пространстве имен. При успешном выполнении этот метод отправляет [**Oncompleteное**](swbemsink-oncompleted.md) событие в объект [**свбемсинк**](swbemsink.md) , указанный в качестве входного параметра.

Этот метод вызывается в асинхронном режиме. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemServicesEx.PutAsync( _
  ByVal objWbemSink, _
  ByVal ojbWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемсинк* 
</dt> <dd>

Обязательный. Приемник объекта, который асинхронно получает объекты. Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.

</dd> <dt>

*ожбвбемобжект* 
</dt> <dd>

Обязательный. Новый объект, помещаемый в пространство имен. Это может быть только что созданный объект или измененный объект.

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Этот параметр определяет, создает ли вызов или обновляет объект, и происходит ли немедленное возвращение вызова. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**вбемчанжефлагупдатекомпатибле** (0 (0x0))


</dt> <dd>

Позволяет обновлять класс при отсутствии производных классов и экземпляров класса. Это также позволяет обновлять во всех случаях, когда изменение выполняется только для неважных квалификаторов, например квалификатор **описания** . Это поведение по умолчанию для этого вызова и используется для совместимости с предыдущими версиями инструментария WMI. Если класс имеет экземпляры, обновление завершается ошибкой.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**вбемчанжефлагупдатесафемоде** (32 (0x20))


</dt> <dd>

Позволяет обновлять классы даже при наличии дочерних классов, а изменение не вызывает конфликтов с дочерними классами. Используйте этот флаг при добавлении нового свойства в базовый класс, который не упоминался ранее в каких-либо дочерних классах. Если класс имеет экземпляры, обновление завершается ошибкой.

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**вбемчанжефлагупдатефорцемоде** (64 (0x40))


</dt> <dd>

Этот флаг вызывает принудительное обновление классов при наличии конфликтующих дочерних классов. Например, этот флаг принудительно выполняет обновление, если квалификатор класса определен в дочернем классе, а базовый класс пытается добавить тот же квалификатор в конфликт с существующим. В принудительном режиме этот конфликт разрешается путем удаления конфликтующего квалификатора в дочернем классе. Если класс имеет экземпляры, обновление завершается ошибкой.

Использование режима Force для обновления статического класса приводит к удалению всех экземпляров этого класса. Принудительное обновление класса поставщика не удаляет экземпляры класса.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**вбемчанжефлагкреатеорупдате** (0 (0x0))


</dt> <dd>

Вызывает создание класса или экземпляра, если он не существует, или перезапись, если он уже существует.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**вбемчанжефлагкреатеонли** (2 (0x2))


</dt> <dd>

Используется только для создания. Вызов завершается ошибкой, если класс или экземпляр уже существует.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**вбемчанжефлагупдатеонли** (1 (0x1))


</dt> <dd>

Приводит к обновлению этого вызова. Для успешного вызова должен существовать класс или экземпляр.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**вбемфлагретурниммедиатели** (16 (0x10))


</dt> <dd>

Приводит к немедленному возврату вызова.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**вбемфлагретурнвхенкомплете** (0 (0x0))


</dt> <dd>

Вызывает блокирование этого вызова до завершения запроса. Этот флаг вызывает метод в синхронном режиме.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**вбемфлагусеамендедкуалифиерс** (131072 (0x20000))


</dt> <dd>

Заставляет Инструментарий WMI записывать данные о поправности классов и определение базового класса. Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> <dt>

*обжвбемасинкконтекст* \[ используемых\]
</dt> <dd>

Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова. Этот параметр используется для выполнения нескольких асинхронных вызовов с использованием одного и того же приемника объекта. Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов. Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) . Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение. Если вызов выполнен успешно, событие [**онобжектпут**](swbemsink-onobjectput.md) переданного приемника объекта получает объект [**свбемобжектпас**](swbemobjectpath.md) , который содержит путь к объекту экземпляра или класса, который успешно зафиксирован в WMI.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **путасинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.

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

Для свойства, которое не может быть равно null, указано значение null. Примером такого свойства является один, помеченный квалификатором **Key**, **индексированного** или **Not \_ null** .

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

Этот вызов возвращает немедленно, а результаты и состояние возвращаются вызывающему через события, доставляемые в приемник, указанный в *обжвбемсинк*. Чтобы обрабатывал каждый объект при поступлении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) . Любая обработка, выполненная после прибытия всех объектов, выполняется в подподпрограмме для *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .

Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник. Это создает угрозы безопасности для сценариев и приложений. Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_ИСВБЕМСЕРВИЦЕСЕКС CLSID<br/>                                                      |
| IID<br/>                      | IID \_ исвбемсервицесекс<br/>                                                        |



 

