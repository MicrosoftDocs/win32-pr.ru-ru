---
description: Метод DELETE \_ объекта SWbemObject удаляет либо текущий класс, либо текущий экземпляр.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: Метод SWbemObject.Delete_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: db8df81e56db9967db46b88c0587af9b82a6281e7e732b8647059e8bf4f5457a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857384"
---
# <a name="swbemobjectdelete_-method"></a>SWbemObject. Delete, \_ метод

Метод **DELETE \_** объекта [**SWbemObject**](swbemobject.md) удаляет либо текущий класс, либо текущий экземпляр. Если динамический поставщик предоставляет класс или экземпляр, то иногда невозможно удалить этот объект, если поставщик не поддерживает удаление класса или экземпляра. Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано и должно быть равно 0 (нулю), если оно указано.

</dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Обычно этот параметр не определен. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **DELETE \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

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

## <a name="remarks"></a>Remarks

Метод **DELETE \_** завершается ошибкой, если создан новый экземпляр [**SWbemObject**](swbemobject.md) , но для ключевого свойства не указано значение. Windows Инструментарий управления (WMI) автоматически создает значение глобального уникального идентификатора (GUID), но значение идентификатора GUID не принимается функцией **SWbemObject. Delete \_**. В этом случае [**SwbemServices. Delete**](swbemservices-delete.md), который использует путь к объекту, работает. Обратите внимание, что объект [**свбемобжектпас**](swbemobjectpath.md) возвращается методом [**SWbemObject \_ .**](swbemobject-put-.md) WHERE после фиксации объекта в WMI.

## <a name="examples"></a>Примеры

В следующем примере создается новый класс. Добавляет свойство ключа; записывает новый класс в репозиторий; и отображает путь к новому объекту класса. Затем скрипт порождает экземпляр нового класса. записывает его; и отображает путь. Обратите внимание, что сценарий удаляет класс и его экземпляры из репозитория, просто удаляя класс.


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



 

 




