---
description: Свойство Privileges является объектом Свбемпривилежесет. Это свойство используется для включения или отключения конкретных привилегий Windows. Может потребоваться установить одно из этих привилегий для выполнения конкретных задач с помощью API инструментарий управления Windows (WMI) (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: Свойство Свбемсекурити. Privileges (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263788"
---
# <a name="swbemsecurityprivileges-property"></a>Свбемсекурити. Privileges, свойство

Свойство **Privileges** является объектом [**свбемпривилежесет**](swbemprivilegeset.md) . Это свойство используется для включения или отключения конкретных привилегий Windows. Может потребоваться установить одно из этих привилегий для выполнения конкретных задач с помощью API инструментарий управления Windows (WMI) (WMI).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Этот параметр позволяет предоставлять или отзывать привилегии как часть строки моникера WMI. Полный список применимых значений см. в разделе константы [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) и [**Privileges**](privilege-constants.md).

Можно изменить привилегии, определенные для объектов [**SwbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**свбемобжектпас**](swbemobjectpath.md)и [**SwbemLocator**](swbemlocator.md) , добавив [**свбемпривилеже**](swbemprivilege.md) объекты в свойство **Privileges** .

Существуют фундаментальные различия в том, как различные версии Windows обрабатывают изменения в привилегиях. Если вы разрабатываете приложение, которое используется только на платформах Windows, вы можете установить или отозвать привилегии в любое время.

В следующем примере задается **SeDebugPrivilege** для первого подключения моникера, чтобы получить объект [**SwbemServices**](swbemservices.md) .


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



Дополнительные сведения о форматировании строки безопасности для подключения моникера см. в разделе [**константы прав**](privilege-constants.md).

В следующем примере выполняется та же задача, но она устанавливает привилегию после первоначального входа в WMI.


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



Обратите внимание, что для вызовов [**свбемпривилежесет. аддасстринг**](swbemprivilegeset-addasstring.md)необходимо использовать полное имя права доступа, например "SeDebugPrivilege", а не "Debug".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМСЕКУРИТИ CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемсекурити<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемсекурити**](swbemsecurity.md)
</dt> <dt>

[Выполнение привилегированных операций](executing-privileged-operations.md)
</dt> <dt>

[**свбемпривилежесет**](swbemprivilegeset.md)
</dt> </dl>

 

 




