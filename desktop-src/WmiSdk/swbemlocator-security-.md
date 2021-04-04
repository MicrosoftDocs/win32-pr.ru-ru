---
description: Свойство безопасности \_ объекта SWbemLocator используется для чтения или установки параметров безопасности объекта SWbemLocator. Это свойство является объектом Свбемсекурити.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: Свойство SWbemLocator.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812419"
---
# <a name="swbemlocatorsecurity_-property"></a>SWbemLocator. Security, \_ свойство

Свойство **безопасности \_** объекта [**SWbemLocator**](swbemlocator.md) используется для чтения или установки параметров безопасности объекта **SWbemLocator** . Это свойство является объектом [**свбемсекурити**](swbemsecurity.md) .

> [!Note]  
> Установка свойства **безопасности \_** объекта [**SWbemLocator**](swbemlocator.md) в **значение NULL** предоставляет всем пользователям неограниченный доступ. Дополнительные сведения см. в разделе [**свбемсекурити**](swbemsecurity.md).

 

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Свойства объекта **SWbemLocator. Security \_** не имеют значений по умолчанию. Если вы попытаетесь получить значение [**свбемсекурити. аусентикатионлевел**](swbemsecurity-authenticationlevel.md) или [**свбемсекурити. Имперсонатионлевел**](swbemsecurity-impersonationlevel.md) в объекте [**SWbemLocator**](swbemlocator.md) , прежде чем приступать к его заданию, возникает ошибка [вбемеррфаилед](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLOCATOR CLSID<br/>                                                          |
| IID<br/>                      | IID \_ исвбемлокатор<br/>                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Создание приложения или скрипта WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Выполнение привилегированных операций с помощью VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Настройка \_ \_ безопасности процесса клиентского приложения](setting-client-application-process-security.md)
</dt> <dt>

[**Объект Свбемсекурити**](swbemsecurity.md)
</dt> <dt>

[Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




