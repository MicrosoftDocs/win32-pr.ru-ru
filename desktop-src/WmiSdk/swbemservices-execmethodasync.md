---
description: Выполняет метод, экспортируемый поставщиком метода.
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Кмесодасинк (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898912efae276fc0404576e162468e06e1b95a68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711625"
---
# <a name="swbemservicesexecmethodasync-method"></a>SWbemServices.Exeметод Кмесодасинк

Метод **ексекмесодасинк** объекта [**SwbemServices**](swbemservices.md) выполняет метод, который экспортируется поставщиком метода. Вызов немедленно возвращается клиенту, в то время как входящие параметры перенаправляются соответствующему поставщику, где выполняется метод. Сведения и состояние возвращаются вызывающему через события, доставляемые в приемник, указанный в *обжвбемсинк*. Поставщик, а не инструментарий управления Windows (WMI) (WMI), реализует метод.

Метод вызывается в асинхронном режиме. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Дополнительные сведения и описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемсинк* 
</dt> <dd>

Обязательный. Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов. Приемник объекта, который получает результат вызова метода. Параметры исходящего трафика отправляются в событие [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) заданного приемника объекта. Результаты механизма вызова отправляются в событие [**свбемсинк. OnComplete**](swbemsink-oncompleted.md) в переданном приемнике объекта. Имейте в виду, что **свбемсинк. OnComplete** не получает код возврата метода WMI. Однако он получает код возврата фактического механизма возврата вызовов, и его удобно использовать только для проверки того, что вызов произошел, или что его не удалось выполнить по механическим причинам. Код результата, возвращаемый из метода WMI, возвращается в объекте исходящего параметра, переданном в **свбемсинк. онобжектреади**. Если возвращается любой код ошибки, указанный объект [**ивбемобжектсинк**](iwbemobjectsink.md) не используется. Если вызов выполнен успешно, то для указания результата операции вызывается реализация **ивбемобжектсинк** пользователя.

</dd> <dt>

*стробжектпас* 
</dt> <dd>

Обязательный. Строка, содержащая путь к объекту, для которого выполняется метод. Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*стрмесоднаме* 
</dt> <dd>

Обязательный. Имя метода, который необходимо выполнить.

</dd> <dt>

*обжвбеминпарамс* \[ используемых\]
</dt> <dd>

Объект [**SWbemObject**](swbemobject.md) , содержащий входные параметры для выполняемого метода. По умолчанию этот параметр не определен. Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

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

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> <dt>

*обжвбемасинкконтекст* \[ используемых\]
</dt> <dd>

Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова. Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта. Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов. Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) . Дополнительные сведения см. в разделе [выполнение асинхронного вызова с помощью VBScript](making-an-asynchronous-call-with-vbscript.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение. Если вызов выполнен успешно, объект [**параметров**](swbemmethod-outparameters.md) , который также является [**SWbemObject**](swbemobject.md) , предоставляется приемнику, указанному в *обжвбемсинк*. Возвращаемый объект **параметров** содержит выходные параметры и возвращаемое значение для выполняемого метода. Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

## <a name="error-codes"></a>Коды ошибок

После завершения метода **ексекмесодасинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок, перечисленных в следующем списке.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

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

</dd> <dt>

**вбемерринвалидмесод** -2147749934 (0x8004102E)
</dt> <dd>

Запрошенный метод недоступен.

</dd> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

Текущий пользователь не имеет разрешения на выполнение метода.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если выполняемый метод имеет входные параметры, то объект с [**параметрами**](swbemmethod-inparameters.md) в параметре *обжвбеминпарам* должен быть таким же, как и описание в разделах конструирование непараметризованных [объектов и синтаксический анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md) .

Используйте **SWbemServices.Exeкмесодасинк** в качестве альтернативы для прямого доступа к [*методу поставщика*](gloss-p.md) , когда невозможно выполнить метод напрямую. Например, используйте его с языком сценариев, который не поддерживает выходные параметры, то есть если метод имеет параметры OUT. В противном случае рекомендуется использовать прямой доступ для вызова метода. Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).

Для метода **SWbemServices.Exeкмесодасинк** требуется путь к объекту. Если скрипт уже содержит объект [**SWbemObject**](swbemobject.md) , можно вызвать метод [**SWbemObject.Exeкмесодасинк**](swbemobject-execmethodasync-.md).

Этот вызов возвращает немедленно. Сведения о состоянии возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*. Чтобы продолжить обработку после завершения вызова, реализуйте подпрограммы для *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .

Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник. Это создает угрозы безопасности для сценариев и приложений. Дополнительные сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).

Используйте параметр *обжвбемасинкконтекст* для проверки источника вызова.

## <a name="examples"></a>Примеры

В следующем примере кода показан метод **ексекмесодасинк** . Скрипт создает объект [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , который представляет процесс, выполняющий программу «Блокнот». Он показывает [**настройку объекта параметров**](swbemmethod-inparameters.md) и способ получения результатов из объекта [**параметров**](swbemmethod-outparameters.md) . Сведения о скрипте, который показывает те же операции, выполняемые синхронно, см. в разделе [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md). Пример использования прямого доступа см. [в разделе Создание метода в классе Win32 \_ процесс](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Пример той же операции с помощью [**SWbemObject**](swbemobject.md)см. в разделе [**SWbemObject.Exeкмесодасинк**](swbemobject-execmethodasync-.md).


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



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

[**SWbemObject.ExeКмесод\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExeКмесодасинк\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExeКмесод**](swbemservices-execmethod.md)
</dt> <dt>

[Вызов метода поставщика](calling-a-provider-method.md)
</dt> <dt>

[Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md)
</dt> </dl>

 

