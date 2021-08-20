---
description: Извлекает экземпляры указанного класса в соответствии с заданным пользователем критерием.
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: SWbemServices. Инстанцесофасинк, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0954f4518d81ea3763fbf4dab0e9e27fde68ab80042c0e192453ef0d5cf983ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921416"
---
# <a name="swbemservicesinstancesofasync-method"></a>SWbemServices. Инстанцесофасинк, метод

Метод **инстанцесофасинк** объекта [**SwbemServices**](swbemservices.md) извлекает экземпляры указанного класса в соответствии с заданным пользователем условием.

Метод вызывается в асинхронном режиме. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемсинк* 
</dt> <dd>

Приемник объекта, который асинхронно получает экземпляры. Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.

</dd> <dt>

*стркласс* 
</dt> <dd>

Обязательный. Строка, содержащая имя класса для нужных экземпляров. Этот параметр не может быть пустым.

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Определяет глубину перечисления вызовов, а также указывает, будет ли вызов немедленно возвращен. Этот параметр может принимать следующие значения.

<dt>

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

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус * * * * (128 (0x80))


</dt> <dd>

Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус * * * * (0 (0x0))


</dt> <dd>

Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс * * * * (131072 (0x20000))


</dt> <dd>

Заставляет WMI возвращать данные о поправности класса с определением базового класса. Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, поддерживающий или требующий сведения о контексте, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> <dt>

*обжвбемасинкконтекст* \[ используемых\]
</dt> <dd>

Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова. Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта. Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов. Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение. В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра. После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **инстанцесофасинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.

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

## <a name="remarks"></a>Remarks

Этот вызов возвращает немедленно. Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*. Чтобы обработать каждый объект при его возврате, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) . После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .

Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник. Это создает угрозы безопасности для сценариев и приложений. Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md) .

Метод **инстанцесофасинк** работает только для объектов класса. Не является ошибкой, когда возвращаемый перечислитель не имеет нулевых (0) элементов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемсервицес<br/>                                                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[Вызов метода](calling-a-method.md)
</dt> </dl>

 

