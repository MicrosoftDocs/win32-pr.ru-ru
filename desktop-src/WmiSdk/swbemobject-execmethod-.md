---
description: Метод ExecMethod \_ объекта SWbemObject выполняет метод, экспортированный поставщиком метода.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: Метод SWbemObject.ExecMethod_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155830"
---
# <a name="swbemobjectexecmethod_-method"></a>SWbemObject.Exe\_ метод кмесод

Метод **ExecMethod \_** объекта [**SWbemObject**](swbemobject.md) выполняет метод, экспортированный поставщиком метода.

Этот метод приостанавливается, пока выполняется метод, перенаправляемый соответствующему поставщику. Затем информация и состояние возвращаются. Поставщик, а не WMI, реализует метод.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стрмесоднаме* \[ окне\]
</dt> <dd>

Обязательный. Имя метода для объекта.

</dd> <dt>

*обжвбеминпарамс* \[ в необязательное\]
</dt> <dd>

Это объект [**SWbemObject**](swbemobject.md) , содержащий входные параметры для выполняемого метода. По умолчанию этот параметр не определен. Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервированное значение и должно быть равно 0 (нуль), если оно задано.

</dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Как правило, он не определен. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод успешно выполнен, объект [**SWbemObject**](swbemobject.md) возвращает. Возвращаемый объект содержит выходные параметры и возвращаемое значение для выполняемого метода.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **ExecMethod \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

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

Этот метод аналогичен [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md), но он работает непосредственно с объектом, метод которого должен быть выполнен. Например, следующий пример кода вызывает метод [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider в [**\_ службе Win32**](/windows/desktop/CIMWin32Prov/win32-service) и использует [прямой доступ](manipulating-class-and-instance-information.md).


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Эта версия вызывает **SWbemObject.Exeкмесод \_** для выполнения метода [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



Используйте **SWbemObject.Exeкмесод \_** в качестве альтернативы прямой доступ для выполнения [*метода поставщика*](gloss-p.md) в случаях, когда невозможно выполнить метод напрямую. Например, можно использовать **SWbemObject.Exeкмесод \_** с языком сценариев, который не поддерживает выходные параметры, если метод имеет параметры out. В противном случае для вызова метода рекомендуется использовать прямой доступ.

-   Метод **SWbemObject.Exeкмесод \_** предполагает, что объект, представленный [**SWbemObject**](swbemobject.md) , содержит метод для выполнения. Напротив, для [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md) требуется путь к объекту. Используйте **SWbemObject.Exeкмесод \_** , если вы уже получили объект, метод которого необходимо выполнить.

## <a name="examples"></a>Примеры

В следующем примере показан метод [**ExecMethod**](swbemservices-execmethod.md) . Скрипт создает объект [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , представляющий процесс, выполняемый в блокноте. Дополнительные сведения о скриптах, иллюстрирующих те же операции, выполняемые асинхронно, см. в разделе [**SWbemObject.Exeкмесодасинк \_**](swbemobject-execmethodasync-.md). Пример использования прямого доступа см. в разделе [**Создание метода в классе Win32 \_ процесс**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Пример той же операции с помощью объекта [**SwbemServices**](swbemservices.md) см. в разделе **SWbemServices.Exeкмесод**.


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
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
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
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
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.ExeКмесодасинк\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExeКмесод**](swbemservices-execmethod.md)
</dt> </dl>

 

