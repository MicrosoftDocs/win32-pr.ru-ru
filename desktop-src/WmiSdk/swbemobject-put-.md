---
description: Метод размещения \_ SWbemObject создает или обновляет экземпляр или объект класса для Инструментарий управления Windows (WMI) (WMI). Этот метод можно использовать после изменения любых свойств или методов в SWbemObject, и ваши изменения записываются в WMI.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: Метод SWbemObject.Put_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f5ca9b79c9def8f209da37e0ef1cfddefa0dbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711643"
---
# <a name="swbemobjectput_-method"></a>SWbemObject. размещение, \_ метод

Метод **размещения \_** [**SWbemObject**](swbemobject.md) создает или обновляет экземпляр или объект класса для Инструментарий управления Windows (WMI) (WMI). Этот метод можно использовать после изменения любых свойств или методов в **SWbemObject**, и ваши изменения записываются в WMI.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Этот параметр определяет, создает ли вызов или обновляет класс или экземпляр, и, если вызов возвращается немедленно. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>Вбемчанжефлагупдатекомпатибле * * * * (0 (0x0))


</dt> <dd>

Позволяет обновлять класс, если нет производных классов и для этого класса нет экземпляров. Это также позволяет обновлять во всех случаях, если изменение относится только к неважным квалификаторам (например, квалификатору **Description** ). Это поведение по умолчанию для этого вызова и используется для совместимости с предыдущими версиями инструментария WMI. Если в классе есть экземпляры, происходит сбой обновления.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>Вбемчанжефлагупдатесафемоде * * * * (32 (0x20))


</dt> <dd>

Позволяет обновлять классы даже при наличии дочерних классов, если изменение не вызывает конфликтов с дочерними классами. Этот флаг можно использовать при добавлении нового свойства в базовый класс, который ранее не упоминался ни в одном из дочерних классов. Если в классе есть экземпляры, происходит сбой обновления. Если в классе есть экземпляры, происходит сбой обновления.

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>Вбемчанжефлагупдатефорцемоде * * * * (64 (0x40))


</dt> <dd>

Этот флаг вызывает принудительное обновление классов при наличии конфликтующих дочерних классов. Например, этот флаг принудительно вызовет обновление, если квалификатор класса был определен в дочернем классе, а базовый класс пытается добавить тот же квалификатор и в конфликт с существующим. В принудительном режиме этот конфликт можно устранить, удалив конфликтующий квалификатор в дочернем классе. Если у класса есть экземпляры, обновление завершится ошибкой.

Использование принудительного режима для обновления статического класса приводит к удалению всех экземпляров этого класса. Принудительное обновление класса поставщика не удаляет экземпляры класса.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>Вбемчанжефлагкреатеорупдате * * * * (0 (0x0))


</dt> <dd>

Вызывает создание класса или экземпляра, если он не существует или перезаписан, если он уже существует.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>Вбемчанжефлагкреатеонли * * * * (0x2)


</dt> <dd>

Используется только для создания. Вызов завершается ошибкой, если класс или экземпляр уже существует.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>Вбемчанжефлагупдатеонли * * * * (1 (0x1))


</dt> <dd>

Приводит к обновлению этого вызова. Для успешного вызова должен существовать класс или экземпляр.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели * * * * (16 (0x10))


</dt> <dd>

Приводит к немедленному возврату вызова.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете * * * * (0 (0x0))


</dt> <dd>

Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс * * * * (131072 (0x20000))


</dt> <dd>

Заставляет Инструментарий WMI записывать данные о поправности классов, а также определение базового класса. Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемобжектпас**](swbemobjectpath.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если вызов выполнен успешно, возвращается объект [**свбемобжектпас**](swbemobjectpath.md) . Этот объект содержит путь к объекту экземпляра или класса, который был успешно передан в WMI.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **размещения \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891
</dt> <dd>

У текущего пользователя нет разрешения на обновление экземпляра указанного класса.

</dd> <dt>

**вбемерралреадексистс** -2147749913 (0x80041019)
</dt> <dd>

Был указан флаг **вбемчанжефлагкреатеонли** , но экземпляр уже существует.

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерриллегалнулл** -2147749898 (0x8004100A)
</dt> <dd>

Для свойства, которое не может быть **Nothing**, указано значение **Nothing** . Примером такого свойства является один, помеченный квалификатором **Key,** **индексированного** или **Not \_ null** .

</dd> <dt>

**вбемерринвалидобжект** -2147749908 (0x80041014)
</dt> <dd>

Задан недопустимый экземпляр.

</dd> <dt>

**вбемерринвалидпараметер** — 0x80041008
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Был указан флаг **вбемчанжефлагупдатеонли** , но экземпляр или класс не существует.

</dd> <dt>

**вбемерринкомплетекласс** -2147749920 (0x80041020)
</dt> <dd>

Обязательные свойства для классов не заданы.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> </dl>

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

[**Свбемобжектпас. класс**](swbemobjectpath-class.md)
</dt> <dt>

[**SWbemProperty**](swbemproperty.md)
</dt> <dt>

[**свбемкуалифиер**](swbemqualifier.md)
</dt> </dl>

 

