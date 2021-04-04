---
description: Метод CompareTo \_ объекта SWbemObject сравнивает два объекта SWbemObject. Это сравнение зависит от определенных ограничений, основанных на значениях, указанных в параметре Ифлагс.
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.tgt_platform: multiple
title: Метод SWbemObject.CompareTo_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.CompareTo_
- ISWbemObject.CompareTo_
- ISWbemObject.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f77bf9db9ee864e136ba695051445e543b466e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812412"
---
# <a name="swbemobjectcompareto_-method"></a>SWbemObject. CompareTo, \_ метод

Метод **CompareTo \_** объекта [**SWbemObject**](swbemobject.md) сравнивает два объекта **SWbemObject** . Это сравнение зависит от определенных ограничений, основанных на значениях, указанных в параметре *ифлагс* .

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемобжект* \[ окне\]
</dt> <dd>

Обязательный. Этот параметр является объектом [**SWbemObject**](swbemobject.md) . Это объект, с которым сравнивается первый объект. Объект должен быть допустимым экземпляром **SWbemObject** .

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Задает характеристики объекта, которые следует учитывать при сравнении объекта с другими объектами. Можно использовать **вбемкомпарисонфлагинклудеалл** , чтобы расдумать все компоненты (это значение по умолчанию) или любое сочетание следующих значений.

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>Вбемкомпарисонфлагинклудеалл * * * * (0 (0x0))


</dt> <dd>

Сравнивает все свойства, квалификаторы и разновидности.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>Вбемкомпарисонфлагигнореобжектсаурце * * * * (0x2)


</dt> <dd>

Приводит к тому, что источник объектов, а именно сервер и пространство имен, из которых они пришли, пропускается в сравнении с другими объектами.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>Вбемкомпарисонфлагигнорекуалифиерс * * * * (1 (0x1))


</dt> <dd>

Приводит к тому, что все квалификаторы (включая **ключ** и **динамический**) будут игнорироваться при сравнении.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>Вбемкомпарисонфлагигноредефаултвалуес * * * * (4 (0x4))


</dt> <dd>

Вызывает игнорирование значений свойств по умолчанию. Этот флаг имеет смысл только при сравнении классов.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>Вбемкомпарисонфлагигнорефлавор * * * * (32 (0x20))


</dt> <dd>

Приводит к игнорированию разновидностей квалификаторов. Этот флаг учитывает значения квалификаторов, но не учитывает различия в разновидностях, например правила распространения и ограничения переопределения.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>Вбемкомпарисонфлагигнорекасе * * * * (16 (0x10))


</dt> <dd>

Сравнивает строковые значения без учета регистра. Это применимо как к строкам, так и к значениям квалификаторов. Имена свойств и квалификаторов всегда сравниваются без учета регистра, независимо от того, установлен данный флаг или нет.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>Вбемкомпарисонфлагигнорекласс * * * * (8 (0x8))


</dt> <dd>

Предписывает системе предположить, что сравниваемые объекты являются экземплярами одного и того же класса. Следовательно, этот флаг сравнивает только сведения, относящиеся к экземпляру. Этот флаг позволяет оптимизировать производительность. Если объекты не являются экземплярами одного класса, результаты будут неопределенными.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает логическое значение **true** , если объекты совпадают. Если объекты не совпадают, возвращается **значение false** .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **CompareTo \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

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
</dt> </dl>

 

 




