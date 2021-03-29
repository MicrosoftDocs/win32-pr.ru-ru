---
description: Свойство Namespace объекта Свбемобжектпас содержит имя пространства имен, которое является частью пути к объекту.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Свойство Свбемобжектпас. Namespace (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 885f7069e901d1d4a490ad7539077463f6c1838c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264996"
---
# <a name="swbemobjectpathnamespace-property"></a>Свбемобжектпас. Namespace, свойство

Свойство **Namespace** объекта [**свбемобжектпас**](swbemobjectpath.md) содержит имя пространства имен, которое является частью пути к объекту. Например, следующий путь показывает свойство Namespace, которое возвращает корневой \\ CIMV2:

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

Описание синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a>Значение свойства

## <a name="examples"></a>Примеры

В следующем примере показано, как получить имя пространства имен из экземпляров [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , которые являются жесткими дисками. Сценарий подключается к пространству имен по умолчанию.


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМОБЖЕКТПАС CLSID<br/>                                                       |
| IID<br/>                      | IID \_ исвбемобжектпас<br/>                                                        |



 

