---
description: Метод Ексекмесодасинк \_ метода SWbemObject асинхронно выполняет метод, который экспортирует поставщик метода.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: Метод SWbemObject.ExecMethodAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37d7a0ab0b2e4d1ab893619eda4b3d32b8b4e1f60791e0981125d4445bda5f98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857354"
---
# <a name="swbemobjectexecmethodasync_-method"></a>SWbemObject.Exe\_ метод кмесодасинк

Метод **ексекмесодасинк \_** метода [**SWbemObject**](swbemobject.md) асинхронно выполняет метод, который экспортирует поставщик метода. Этот метод аналогичен [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md), но работает непосредственно с объектом метода для выполнения. Windows Инструментарий управления (WMI) не реализует этот метод. Поставщик реализует этот метод.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемсинк* \[ окне\]
</dt> <dd>

Обязательный. Это приемник объекта, который получает результаты вызова метода. Параметры исходящего трафика отправляются в событие [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) заданного приемника объекта. Результаты механизма вызова отправляются в событие [**свбемсинк. OnComplete**](swbemsink-oncompleted.md) в переданном приемнике объекта. Обратите внимание, что **свбемсинк. OnComplete** не получает код возврата метода. Однако он получает код возврата фактического механизма возврата вызовов, и его удобно использовать только для проверки того, что вызов произошел, или его сбой по механическим причинам. Код результата, возвращенный методом, возвращается в объекте исходящего параметра, переданном в **свбемсинк. онобжектреади**. Если код ошибки возвращается, указанный объект [**ивбемобжектсинк**](iwbemobjectsink.md) не используется. Если вызов выполнен успешно, то для указания результата операции вызывается реализация **ивбемобжектсинк** пользователя.

</dd> <dt>

*стрмесоднаме* \[ окне\]
</dt> <dd>

Обязательный. Это имя метода для объекта.

</dd> <dt>

*обжвбеминпарамс* \[ в необязательное\]
</dt> <dd>

Это объект [**SWbemObject**](swbemobject.md) , содержащий входные параметры для выполняемого метода. По умолчанию этот параметр не определен. Дополнительные сведения см. в разделе [Построение объектов параметров](constructing-inparameters-objects.md) и [анализ объектов параметров](parsing-outparameters-objects.md).

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Целое число, определяющее поведение вызова. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус * * * * (128 (0x80))


</dt> <dd>

Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**свбемсинк. OnProgress**](swbemsink-onprogress.md) для приемника объекта.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус * * * * (0 (0x0))


</dt> <dd>

Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Как правило, он не определен. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> <dt>

*обжвбемасинкконтекст* \[ в необязательное\]
</dt> <dd>

Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова. Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта. Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов. Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) . Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не имеет возвращаемых значений. Если вызов выполнен успешно, объект [**параметров**](swbemmethod-outparameters.md) , который также является объектом [**SWbemObject**](swbemobject.md) , предоставляется приемнику, указанному в *обжвбемсинк*. Возвращаемый объект **параметров** содержит выходные параметры и возвращаемое значение для выполняемого метода.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **ексекмесодасинк \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.

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

## <a name="remarks"></a>Remarks

Используйте **SWbemObject.Exeметод кмесодасинк \_** в качестве альтернативы для прямого доступа к [*методу поставщика*](gloss-p.md) , когда невозможно выполнить метод напрямую. Например, если метод имеет выходные параметры, используйте метод **SWbemObject.Exeкмесодасинк \_** с языком сценариев, который не поддерживает выходные параметры. В противном случае рекомендуется вызывать метод с помощью прямого доступа. Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).

Этот вызов возвращает немедленно. Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*. Чтобы обработать каждый объект при поступлении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) . После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .

Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник. Это создает угрозы безопасности для сценариев и приложений. Чтобы устранить риски, используйте либо семисинчронаус связь, либо синхронное взаимодействие. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Если выполняемый метод имеет входные параметры, необходимо создать объект [**параметров**](swbemmethod-inparameters.md) и параметр *обжвбеминпарам* , как описано в разделе [Создание объектов параметров](constructing-inparameters-objects.md) и [анализ объектов параметров](parsing-outparameters-objects.md).

Метод **SWbemObject.Exeкмесодасинк \_** предполагает, что объект, представленный [**SWbemObject**](swbemobject.md) , содержит метод для выполнения. Для метода [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md) требуется путь к объекту.

## <a name="examples"></a>Примеры

В следующем примере показан метод [**ексекмесодасинк**](swbemservices-execmethodasync.md) . скрипт создает объект [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , который представляет процесс, выполняющий Блокнот. Он показывает, как настроить [**объект параметров**](swbemmethod-inparameters.md) и как получить результаты из объекта [**параметров**](swbemmethod-outparameters.md) .

Сведения о скрипте, который показывает те же операции, выполняемые синхронно, см. в разделе [**SWbemObject.Exeкмесод**](swbemobject-execmethod-.md). Пример использования прямого доступа см. в разделе [**Создание метода в классе Win32 \_ процесс**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Пример той же операции с помощью объекта [**SwbemServices**](swbemservices.md) см. в разделе [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md).


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
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
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemServices.ExeКмесодасинк**](swbemservices-execmethodasync.md)
</dt> </dl>

 

