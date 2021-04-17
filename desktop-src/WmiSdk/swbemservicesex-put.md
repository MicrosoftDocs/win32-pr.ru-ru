---
description: Возвращает объект Свбемобжектпас, содержащий путь к объекту, в который были записаны данные.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: Метод Свбемсервицесекс. Where (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711618"
---
# <a name="swbemservicesexput-method"></a>Свбемсервицесекс. размещение, метод

Метод **размещения** объекта [**свбемсервицесекс**](swbemservicesex.md) сохраняет объект в пространство имен, привязанное к объекту, и возвращает объект [**свбемобжектпас**](swbemobjectpath.md) , содержащий путь к объекту, в который были записаны данные.

Этот метод вызывается в режиме семисинчронаус. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемобжект* 
</dt> <dd>

Обязательный. Новый объект, помещаемый в пространство имен. Это может быть только что созданный объект или измененный объект.

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Этот параметр определяет, создает ли вызов или обновляет объект, и, если вызов возвращается немедленно. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**вбемчанжефлагупдатекомпатибле** (0 (0x0))


</dt> <dd>

Позволяет обновлять класс, если нет производных классов и для этого класса нет экземпляров. Это также позволяет обновлять во всех случаях, если изменение относится только к неважным квалификаторам (например, квалификатору **Description** ). Это поведение по умолчанию для этого вызова и используется для совместимости с предыдущими версиями инструментария WMI. Если класс имеет экземпляры, обновление завершается ошибкой.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**вбемчанжефлагупдатесафемоде** (32 (0x20))


</dt> <dd>

Позволяет обновлять классы даже при наличии дочерних классов, если изменение не вызывает конфликтов с дочерними классами. Этот флаг можно использовать при добавлении нового свойства в базовый класс, который ранее не упоминался ни в одном из дочерних классов. Если класс имеет экземпляры, обновление завершается ошибкой.

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**вбемчанжефлагупдатефорцемоде** (64 (0x40))


</dt> <dd>

Этот флаг вызывает принудительное обновление классов при наличии конфликтующих дочерних классов. Например, этот флаг приводит к принудительному обновлению, если квалификатор класса был определен в дочернем классе, а базовый класс пытается добавить тот же квалификатор в конфликт с существующим. В принудительном режиме этот конфликт разрешается путем удаления конфликтующего квалификатора в дочернем классе. Если класс имеет экземпляры, обновление завершается ошибкой.

Использование режима Force для обновления статического класса приводит к удалению всех экземпляров этого класса. Принудительное обновление класса поставщика не удаляет экземпляры класса.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**вбемчанжефлагкреатеорупдате** (0 (0x0))


</dt> <dd>

Вызывает создание класса или экземпляра, если он не существует, или перезапись, если он уже существует.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**вбемчанжефлагкреатеонли** (2 (0x2))


</dt> <dd>

Используется только для создания. Вызов завершается ошибкой, если класс или экземпляр уже существует.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**вбемчанжефлагупдатеонли** (1 (0x1))


</dt> <dd>

Вызывает выполнение этого вызова только для обновления. Для успешного вызова должен существовать класс или экземпляр.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**вбемфлагретурниммедиатели** (16 (0x10))


</dt> <dd>

Приводит к немедленному возврату вызова.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**вбемфлагретурнвхенкомплете** (0 (0x0))


</dt> <dd>

Вызывает блокирование этого вызова до завершения операции. Этот флаг вызывает метод в синхронном режиме.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**вбемфлагусеамендедкуалифиерс** (131072 (0x20000))


</dt> <dd>

Заставляет Инструментарий WMI записывать данные о поправности классов, а также определение базового класса. Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если вызов выполнен успешно, возвращается объект [**свбемобжектпас**](swbemobjectpath.md) . Этот объект содержит путь к объекту экземпляра или класса, который был успешно передан в WMI.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **размещения** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

У текущего пользователя нет разрешения на операцию.

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

Для свойства, которое не может быть **равно NULL**, указано значение **null** . Примером такого свойства является один, помеченный квалификатором [**Key**](standard-qualifiers.md), **индексированного** или **Not \_ null** .

</dd> <dt>

**вбемерринвалидобжект** -2147749908 (0x80041014)
</dt> <dd>

Указан недопустимый объект.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
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
| CLSID<br/>                    | \_ИСВБЕМСЕРВИЦЕСЕКС CLSID<br/>                                                      |
| IID<br/>                      | IID \_ исвбемсервицесекс<br/>                                                        |



 

 




