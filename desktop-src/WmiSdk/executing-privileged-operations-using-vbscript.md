---
description: При использовании API скриптов для WMI можно задать определенные привилегии безопасности.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Выполнение привилегированных операций с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156822"
---
# <a name="executing-privileged-operations-using-vbscript"></a>Выполнение привилегированных операций с помощью VBScript

При использовании API скриптов для WMI можно задать определенные привилегии безопасности. Например, можно задать привилегии безопасности для запроса завершения работы операционной системы или проверить журнал событий безопасности. Дополнительные сведения см. [в разделе выполнение с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).

При доступе к инструментарию WMI на компьютере необходимо установить только привилегии. При обращении к удаленному узлу COM RPC автоматически устанавливает привилегии. Чтобы определить все необходимые привилегии, обратитесь к документации по конкретным классам WMI, к которым вы хотите получить доступ, например Win32 с именем [**\_ операционной**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)системы. Дополнительные сведения см. в разделе [вбемпривилежеенум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)

В этом разделе обсуждаются следующие разделы:

-   [Установка привилегий из объекта безопасности \_](/windows)
-   [Настройка привилегий как части моникера](#setting-a-privilege-as-part-of-a-moniker)
-   [Отмена и сброс привилегий](#revoking-and-resetting-privileges)
-   [См. также](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a>Установка привилегий из объекта безопасности \_

Используйте следующую процедуру, чтобы задать привилегии безопасности в Visual Basic.

**Установка привилегий в Visual Basic**

1.  Создайте объект типа [**SWbemLocator**](swbemlocator.md).
2.  Добавьте новую привилегию в объект [**SWbemLocator. Security \_**](swbemlocator-security-.md) .

    Объект [**безопасности \_**](swbemlocator-security-.md) содержит коллекцию [**SWbemObjectSet**](swbemobjectset.md) . Объекты в наборе являются объектами [**свбемсекурити**](swbemsecurity.md) . Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).

3.  Войдите в WMI и получите объект [**SwbemServices**](swbemservices.md) .

    Объект [**SwbemServices**](swbemservices.md) наследует привилегию, заданную на предыдущем шаге.

Вы также можете задать привилегию с помощью метода [**свбемпривилежесет. аддасстринг**](swbemprivilegeset-addasstring.md) .

## <a name="setting-a-privilege-as-part-of-a-moniker"></a>Настройка привилегий как части моникера

Вы можете задать привилегию как часть моникера.

В следующем примере показано, как добавить в моникер привилегию отладки.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a>Отмена и сброс привилегий

В следующем примере показано, как задать привилегию **SeDebugPrivilege** и отозвать привилегию **серемотешутдовнпривилеже** .


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Константы прав доступа**](privilege-constants.md)
</dt> <dt>

[Выполнение привилегированных операций](executing-privileged-operations.md)
</dt> </dl>

 

 
