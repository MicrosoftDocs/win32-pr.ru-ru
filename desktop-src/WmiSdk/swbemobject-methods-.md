---
description: Свойство Methods \_ объекта SWbemObject возвращает объект свбеммесодсет, который является коллекцией методов для текущего класса или экземпляра. Это свойство доступно только для чтения.
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: Свойство SWbemObject.Methods_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0442798a7630de20ff062a631baa335c5f6ed960900d571ca1d0e9e9a067f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991984"
---
# <a name="swbemobjectmethods_-property"></a>SWbemObject. Methods, \_ свойство

Свойство **Methods \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**свбеммесодсет**](swbemmethodset.md) , который является коллекцией методов для текущего класса или экземпляра. Это свойство доступно только для чтения.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="examples"></a>Примеры

Следующий [пример кода](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), взятый из коллекции TechNet, описывает, как перечислить все методы класса.


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
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



 

 




