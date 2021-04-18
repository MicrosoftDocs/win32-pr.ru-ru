---
description: Удаляет класс или экземпляр, указанный в пути объекта. Удалять можно только объекты из текущего пространства имен.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Метод SWbemServices. Delete (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497835"
---
# <a name="swbemservicesdelete-method"></a>SWbemServices. Delete, метод

Метод **Delete** объекта [**SwbemServices**](swbemservices.md) удаляет класс или экземпляр, указанный в пути объекта. Удалять можно только объекты из текущего пространства имен.

Если динамический поставщик предоставляет класс или экземпляр, удалить этот объект нельзя, если поставщик не поддерживает удаление класса или экземпляра.

Этот метод вызывается в синхронном режиме. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стробжектпас* 
</dt> <dd>

Обязательный. Строка, содержащая путь к объекту, который необходимо удалить. Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Зарезервировано. Это значение должно быть равно нулю.

</dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Delete** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

Текущий контекст не имеет достаточных прав безопасности для удаления объекта.

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидкласс** -2147749904 (0x80041010)
</dt> <dd>

Указанный класс не существует.

</dd> <dt>

**вбемерринвалидоператион** -2147749910 (0x80041016)
</dt> <dd>

Не удается удалить объект.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Объект не существует.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Метод **SwbemServices. Delete** может использоваться, когда свойству ключа объекта не присвоено значение, так как для этого метода в качестве входных данных требуется только путь к объекту. Этот метод можно использовать в ситуациях, когда [**SWbemObject. Delete \_**](swbemobject-delete-.md) завершается неудачей для отсутствия значения ключа. Если объект зафиксирован в WMI с помощью [**SWbemObject. \_ постановки**](swbemobject-put-.md), объект [**свбемобжектпас**](swbemobjectpath.md) был получен через вызов.

## <a name="examples"></a>Примеры

В следующем примере создается новый класс, добавляется свойство, которое не является ключом, записывает новый класс в репозиторий и отображает путь к новому объекту класса. Затем скрипт порождает экземпляр нового класса, записывает экземпляр и отображает путь. Обратите внимание, что скрипт удаляет класс и его экземпляры из репозитория, удаляя класс. Дополнительные сведения о классах и экземплярах WMI см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md) и [модель CIM](common-information-model.md).


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
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

[**свбемобжектпас**](swbemobjectpath.md)
</dt> </dl>

 

 




