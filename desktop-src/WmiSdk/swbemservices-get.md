---
description: Извлекает объект, который является либо определением класса, либо экземпляром на основе пути к объекту.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: Метод SWbemServices. Get (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8998a1ca04206362fcc0e7405fccf8c923d74d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712100"
---
# <a name="swbemservicesget-method"></a>SWbemServices. Get, метод

Метод **Get** объекта [**SwbemServices**](swbemservices.md) извлекает объект, который является либо определением класса, либо экземпляром на основе пути к объекту. Этот метод извлекает только объекты из пространства имен, связанного с текущим объектом **SwbemServices** .

Метод вызывается в синхронном режиме. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стробжектпас* \[ используемых\]
</dt> <dd>

Строка, содержащая путь к объекту объекта для извлечения. Если это значение пустое, возвращаемый пустой объект может стать новым классом. Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Целое число, определяющее поведение запроса. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс * * * * (131072 (0x20000))


</dt> <dd>

Заставляет WMI возвращать данные о поправности класса с определением базового класса. Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения этот метод возвращает объект [**SWbemObject**](swbemobject.md) , представляющий запрошенный объект.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Get** объект **Err** может содержать один из кодов ошибок из следующего списка.

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

В отличие от методов [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) и [**Инстанцесоф**](swbemservices-instancesof.md) , метод Get всегда возвращает [**SWbemObject**](swbemobject.md) , представляющий конкретный экземпляр управляемого WMI ресурса. Чтобы получить конкретный экземпляр управляемого WMI ресурса с помощью метода Get, необходимо определить получение экземпляра, передав методу путь к объекту, как показано в следующем скрипте.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



Этот метод можно использовать для получения [*одноэлементных*](gloss-s.md) объектов, таких как [**\_ \_ Цимомидентификатион**](--cimomidentification.md), которые содержат сведения о версии установленного WMI.

Вы можете проверить репозиторий с помощью средства просмотра, такого как [CIM Studio](further-information.md) , чтобы убедиться, что появился новый класс и экземпляр. Пример удаления класса и экземпляра из репозитория см. в разделе [**SwbemServices. Delete**](swbemservices-delete.md) или [**\_ SWbemObject. Delete**](swbemobject-delete-.md).

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

 

 




