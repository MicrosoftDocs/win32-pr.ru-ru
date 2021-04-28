---
description: SWbemServices.Exeметод Ккуери — выполняет запрос для получения объектов.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Ккуери (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3009d2dc88e9987a3559da91eed1aa5aa1b248f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098341"
---
# <a name="swbemservicesexecquery-method"></a>SWbemServices.Exeметод Ккуери

Метод **ExecQuery** объекта [**SwbemServices**](swbemservices.md) выполняет запрос для получения объектов. Эти объекты доступны через возвращенную коллекцию [**SWbemObjectSet**](swbemobjectset.md) .

Этот метод вызывается в режиме семисинчронаус. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стркуери* 
</dt> <dd>

Обязательный элемент. Строка, содержащая текст запроса. Этот параметр не может быть пустым. Дополнительные сведения о создании строк запросов WMI см. в разделе [запросы с помощью WQL](querying-with-wql.md) и Справочник по [WQL](wql-sql-for-wmi.md) .

</dd> <dt>

*стркуерилангуаже* \[ используемых\]
</dt> <dd>

Строка, содержащая используемый язык запросов. Если указано, это значение должно быть "WQL".

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Целое число, определяющее поведение запроса и определяющее, будет ли этот вызов немедленно возвращен. Значение этого параметра по умолчанию — **вбемфлагретурниммедиатели**. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли * * * * (32 (0x20))


</dt> <dd>

Вызывает возврат перечислителя "только вперед". Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал * * * * (0 (0x0))


</dt> <dd>

Заставляет Инструментарий WMI хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели * * * * (16 (0x10))


</dt> <dd>

Приводит к немедленному возврату вызова.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете * * * * (0 (0x0))


</dt> <dd>

Вызывает блокирование этого вызова до завершения запроса. Этот флаг вызывает метод в синхронном режиме.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>Вбемкуерифлагпрототипе * * * * (0x2)


</dt> <dd>

Используется для создания прототипов. Этот флаг останавливает запрос и возвращает объект, который выглядит как типичный объект результата.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс * * * * (131072 (0x20000))


</dt> <dd>

Заставляет WMI возвращать данные о поправности класса с определением базового класса. Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если ошибка не возникает, этот метод возвращает объект [**SWbemObjectSet**](swbemobjectset.md) . Это коллекция объектов, содержащая результирующий набор запроса. Вызывающий объект может проверить коллекцию, используя реализацию коллекций для используемого языка программирования. Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).

## <a name="error-codes"></a>Коды ошибок

После завершения метода **ExecQuery** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

У текущего пользователя нет разрешения на Просмотр результирующего набора.

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемерринвалидкуери** -2147749911 (0x80041017)
</dt> <dd>

Недопустимый синтаксис запроса.

</dd> <dt>

**вбемерринвалидкуеритипе** -2147749912 (0x80041018)
</dt> <dd>

Запрошенный язык запросов не поддерживается.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> </dl>

## <a name="remarks"></a>Remarks

**ExecQuery** — один из наиболее часто используемых вызовов для получения сведений WMI. Стандартный вызов **ExecQuery** выглядит следующим образом:


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



Обратите внимание, что вы создаете объект [**SwbemServices**](swbemservices.md) с моникером, который представляет соответствующее пространство имен и безопасность, а затем делает вызов **ExecQuery** через службу. Более подробное обсуждение см. в разделе [Создание скрипта WMI](creating-a-wmi-script.md) и [перечисление WMI](enumerating-wmi.md).

Как и метод [**инстанцесоф**](swbemservices-instancesof.md) , метод **ExecQuery** всегда возвращает коллекцию [**SWbemObjectSet**](swbemobjectset.md) . Таким образом, сценарий WMI должен перечислить коллекцию ExecQuery, чтобы получить доступ к каждому экземпляру управляемого ресурса в коллекции, как показано ниже:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Другие методы [**SwbemServices**](swbemservices.md) , возвращающие [**SWbemObjectSet**](swbemobjectset.md) , включают [**ассоЦиаторсоф**](swbemservices-associatorsof.md), [**референцесто**](swbemservices-referencesto.md)и [**субклассесоф**](swbemservices-subclassesof.md).

Запрос на возврат пустого результирующего набора не является ошибкой. Метод **ExecQuery** возвращает ключевые свойства независимо от того, запрашивается ли ключевое свойство в аргументе *стркуери* . Если при выполнении этого метода возникает ошибка и не используется флаг **вбемфлагретурниммедиатели** , то объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) не задается до тех пор, пока не будет произведена попытка получить доступ к возвращенному набору объектов. Однако при использовании флага **вбемфлагретурнвхенкомплете** объект Err задается при вызове метода **ExecQuery** .

Существует ряд ограничений на количество ключевых слов **and** и **or** , которые могут использоваться в запросах WQL. Большое количество ключевых слов WQL, используемых в сложном запросе, может привести к тому, что WMI вернет код ошибки **\_ \_ \_ нарушения квоты WBEM E** как значение **HRESULT** . Ограничение ключевых слов WQL зависит от того, насколько сложным является запрос.

## <a name="examples"></a>Примеры

Следующий пример кода VBScript находит все диски на локальном компьютере и отображает идентификатор устройства и тип диска.


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
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



## <a name="see-also"></a>См. также

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemServices. Get**](swbemservices-get.md)
</dt> <dt>

[Запросы с помощью WQL](querying-with-wql.md)
</dt> <dt>

[Создание скрипта WMI](creating-a-wmi-script.md)
</dt> <dt>

[Перечисление WMI](enumerating-wmi.md)
</dt> </dl>

 

