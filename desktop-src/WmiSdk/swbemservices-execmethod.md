---
description: Выполняет метод, экспортируемый поставщиком метода.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Кмесод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c95bc3b0fa85d7c682f9ffd2436439da9a05763f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080892"
---
# <a name="swbemservicesexecmethod-method"></a>SWbemServices.Exeметод Кмесод

Метод **ExecMethod** объекта [**SwbemServices**](swbemservices.md) выполняет метод, экспортируемый поставщиком метода. Этот метод блокируется, пока выполняется метод, перенаправляемый соответствующему поставщику. Затем информация и состояние возвращаются. Поставщик, а не WMI, реализует метод.

Этот метод вызывается в синхронном режиме. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стробжектпас* 
</dt> <dd>

Обязательный. Строка, содержащая путь к объекту, для которого выполняется метод. Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*стрмесоднаме* 
</dt> <dd>

Обязательный. Имя метода для объекта.

</dd> <dt>

*обжвбеминпарамс* \[ используемых\]
</dt> <dd>

Объект [**SWbemObject**](swbemobject.md) , содержащий входные параметры для выполняемого метода. По умолчанию этот параметр не определен. Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Зарезервировано. Это значение должно быть равно нулю.

</dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается объект [**SWbemObject**](swbemobject.md) . Возвращаемый объект содержит выходные параметры и возвращаемое значение для выполняемого метода.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **ExecMethod** объект **Err** может содержать один из кодов ошибок из следующего списка.

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

Используйте **SWbemServices.Exeкмесод** в качестве альтернативы прямой доступ для выполнения [*метода поставщика*](gloss-p.md) в случаях, когда невозможно выполнить метод напрямую. Метод **ExecMethod** позволяет получать выходные параметры, если поставщик предоставляет их, с языком сценариев, который не поддерживает выходные параметры. В противном случае для вызова метода рекомендуется использовать прямой доступ. Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).

Например, следующий пример кода, вызывающий метод [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider в [**\_ службе Win32**](/windows/desktop/CIMWin32Prov/win32-service) , использует прямой доступ.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



В этом примере вызывается **SWbemServices.Exeкмесод** для выполнения метода [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) . Обратите внимание, что путь к объекту необходим, так как **SWbemServices.Exeкмесод** не работает над объектом, в отличие от [**SWbemObject.Exeкмесод**](swbemobject-execmethod-.md).


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



Для метода **SWbemServices.Exeкмесод** требуется путь к объекту. Если в скрипте уже содержится объект [**SWbemObject**](swbemobject.md) , используйте метод [**SWbemObject.Exeкмесод**](swbemobject-execmethod-.md) .

## <a name="examples"></a>Примеры

В следующем примере показан метод **ExecMethod** . Скрипт создает объект [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , который представляет процесс, выполняющий программу «Блокнот». Он показывает [**настройку объекта параметров**](swbemmethod-inparameters.md) и способ получения результатов из объекта [**параметров**](swbemmethod-outparameters.md) . Сведения о скрипте, отображающем те же операции, выполняемые асинхронно, см. в разделе [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md). Пример использования прямого доступа см. [в разделе Создание метода в классе Win32 \_ процесс](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Пример той же операции с помощью [**SWbemObject**](swbemobject.md)см. в разделе [**SWbemObject.Exeкмесод**](swbemobject-execmethod-.md).


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
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

[Вызов метода поставщика](calling-a-provider-method.md)
</dt> <dt>

[Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md)
</dt> </dl>

 

