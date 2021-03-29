---
description: Извлекает объект, который является определением класса или экземпляром, на основе пути к объекту.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: Метод SWbemServices. async (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898529"
---
# <a name="swbemservicesgetasync-method"></a>SWbemServices. async, метод

Метод **Async** объекта [**SwbemServices**](swbemservices.md) извлекает объект, который является определением класса или экземпляром, на основе пути к объекту.

Этот метод извлекает только объекты из пространства имен, связанного с текущим объектом [**SwbemServices**](swbemservices.md) .

Этот метод вызывается в асинхронном режиме. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемсинк* 
</dt> <dd>

Обязательный. Приемник объекта, который получает объекты асинхронно. Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.

</dd> <dt>

*стробжектпас* \[ используемых\]
</dt> <dd>

Путь к объекту, который требуется получить. Если это значение пустое, возвращаемый пустой объект может стать новым классом. Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Целое число, определяющее поведение вызова. Этот параметр может принимать следующие значения.

<dt>

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

Как правило, это значение не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> <dt>

*обжвбемасинкконтекст* \[ используемых\]
</dt> <dd>

Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова. Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта. Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов. Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) . Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение. В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) , когда объект доступен.

## <a name="error-codes"></a>Коды ошибок

После завершения метода с методом **Async** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

У текущего пользователя нет разрешения на доступ к объекту.

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемерринвалидобжектпас** -2147749946 (0x8004103A)
</dt> <dd>

Указан недопустимый путь.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Не удалось найти запрошенный объект.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот вызов возвращает немедленно. Запрошенный объект и состояние возвращаются вызывающему через обратный вызов, доставленный в приемник, указанный в *обжвбемсинк*. Чтобы обработать объект при его возврате, создайте *обжвбемсинк*. [**Онобжектреади**](swbemsink-onobjectready.md)или *обжвбемсинк*. Подпрограммы [**Oncompleteed**](swbemsink-oncompleted.md) Event.

Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник. Это создает угрозы безопасности для сценариев и приложений. Чтобы устранить риски, используйте семисинчронаус или синхронный обмен данными. Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).

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

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

