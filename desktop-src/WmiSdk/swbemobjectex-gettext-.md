---
description: Возвращает XML-представление объекта или экземпляра. Текстовый файл форматируется в формате XML, указанном, как показано в Вбемобжекттекстформатенум.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: Метод SWbemObjectEx.GetText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a75adbab65c735a298c6a1599718cc6df5b690dd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623330"
---
# <a name="swbemobjectexgettext_-method"></a>Свбемобжектекс. GetText, \_ метод

Метод **gettext \_** объекта [**свбемобжектекс**](swbemobjectex.md) возвращает XML-представление объекта или экземпляра. Текстовый файл форматируется в формате XML, указанном, как показано в [**вбемобжекттекстформатенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*итекстформат* \[ окне\]
</dt> <dd>

Обязательный. Значение из [**вбемобжекттекстформатенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) , указывающее результирующий формат XML.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Флаги зарезервированных операций. Значение по умолчанию — 0 (нуль).

</dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который задает контекст для операции. Значение по умолчанию — NULL. Дополнительные сведения о разрешенных парах "имя-значение" см. в разделе "Примечания" ниже.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не имеет возвращаемых значений.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **gettext \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Запрошенный формат не найден.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Один из параметров вызова указан неправильно.

</dd> <dt>

**вбемерркритикалеррор** -2147749898 (0x8004100A)
</dt> <dd>

Произошла внутренняя, критическая, неожиданная ошибка. Отправьте отчет об этой ошибке в службу технической поддержки корпорации Майкрософт.

</dd> </dl>

## <a name="remarks"></a>Remarks

При создании [**свбемнамедвалуесет**](swbemnamedvalueset.md)допускаются только следующие пары "имя-значение".



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Имя</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LocalOnly</td>
<td><strong>VT_BOOL</strong><br/> Если <strong>значение — true</strong>, в результирующем XML-коде есть только локально определенные свойства и методы. Значение по умолчанию — <strong>false</strong>.<br/></td>
</tr>
<tr class="even">
<td>инклудекуалифиерс</td>
<td><strong>VT_BOOL</strong><br/> Если <strong>значение равно true</strong>, квалификаторы классов, экземпляров, свойств и методов включаются в результирующий XML. Значение по умолчанию — <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td>паслевел</td>
<td><strong>VT-I4</strong><br/> Значение по умолчанию — 0 (ноль). Возможны следующие значения:<br/>
<ul>
<li>0: <CLASS> элемент OR <INSTANCE> создается в зависимости от того, является ли объект классом или экземпляром.</li>
<li>1: <VALUE.NAMEDOBJECT> создается элемент.</li>
<li>2: <VALUE.OBJECTWITHLOCALPATH> создается элемент.</li>
<li>3: <VALUE.OBJECTWITHPATH> создается элемент.</li>
</ul></td>
</tr>
<tr class="even">
<td>ексклудесистемпропертиес</td>
<td><strong>VT-BOOL</strong><br/> Если <strong>значение — true</strong>, системные свойства, такие как __NAMESPACE, исключаются из выходных данных.<br/></td>
</tr>
<tr class="odd">
<td>инклудеклассоригин</td>
<td><strong>VT_BOOL</strong><br/> Если <strong>значение — true</strong>, атрибут начала класса задается <PROPERTY> для <METHOD> элементов и. Значение по умолчанию — <strong>false</strong>.<br/></td>
</tr>
</tbody>
</table>



 

Дополнительные сведения о создании [**свбемнамедвалуесет**](swbemnamedvalueset.md)см. в разделе [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md).

## <a name="examples"></a>Примеры

В следующем сценарии показано, как получить XML-представление определения класса [**\_ BIOS Win32**](/windows/desktop/CIMWin32Prov/win32-bios) . Указав определенный экземпляр **Win32 \_ BIOS**, можно получить данные этого объекта в формате XML.


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМОБЖЕКТЕКС CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемобжектекс<br/>                                                          |



 

