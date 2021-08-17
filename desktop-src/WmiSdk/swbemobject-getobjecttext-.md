---
description: Метод Жетобжекттекст \_ объекта SWbemObject Возвращает текстовое представление объекта.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: Метод SWbemObject.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d33e4f3f530bf7d9bda2e228243026de7d3768efb668cf6c8683690e8127f65f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992064"
---
# <a name="swbemobjectgetobjecttext_-method"></a>SWbemObject. Жетобжекттекст, \_ метод

Метод **жетобжекттекст \_** объекта [**SWbemObject**](swbemobject.md) Возвращает текстовое представление объекта. Этот объект можно использовать для вывода содержимого объекта. В настоящее время в качестве выходного формата поддерживается только синтаксис MOF. Обратите внимание, что возвращенный текст MOF не содержит все сведения об объекте; MOF-текст содержит достаточно информации, чтобы компилятор MOF мог создать исходный объект заново. Например, отсутствуют сведения о распространяемых квалификаторах или свойствах родительского класса.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано и должно быть равно 0 (нулю), если оно указано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха этот метод возвращает строку, содержащую выходной текст.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **жетобжекттекст \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

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

## <a name="examples"></a>Примеры

Следующий код, взятый из [списка определения класса WMI в формате MOF в виде](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) кода VBScript в коллекции TechNet, извлекает и отображает текстовое представление определения класса WMI в синтаксисе MOF (MOF-файл).


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
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



 

 




