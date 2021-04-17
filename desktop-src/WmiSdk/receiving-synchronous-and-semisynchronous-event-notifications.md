---
description: Используйте SWbemServices.ExeКкуери, чтобы запросить все существующие события.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Получение синхронных и Семисинчронаус уведомлений о событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693270"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a>Получение синхронных и Семисинчронаус уведомлений о событиях

Используйте [**SWbemServices.Exeккуери**](swbemservices-execquery.md) , чтобы запросить все существующие события.

В следующем примере кода показано, как запросить события в журнале.

`Select * from Win32_NTLogEvent`

Дополнительные сведения см. в статьях [Определение типа получаемого события](determining-the-type-of-event-to-receive.md), [Получение уведомлений о событиях](receiving-event-notifications.md)и [WQL (SQL для WMI)](wql-sql-for-wmi.md).

При вызове [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) по умолчанию используется обмен данными семисинчронаус. По умолчанию для параметра *ифлагс* заданы флаги **вбемфлагфорвардонли** и **вбемфлагретурниммедиатели** . Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

В следующей процедуре описывается получение уведомления о событии семисинчронаус с помощью VBScript.

**Получение уведомления о событии семисинчронаус в VBScript**

1.  Создайте запрос для типа события, которое требуется получить. Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).

2.  Если вы запрашиваете тип экземпляра события, например [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md), укажите в запросе тип целевого экземпляра, например [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).

3.  При необходимости укажите экземпляр, например имя пространства имен при запросе будущих экземпляров [**\_ \_ намеспацемодификатионевент**](--namespacemodificationevent.md) для определенного пространства имен.

4.  Укажите интервал опроса для инструментарий управления Windows (WMI) (WMI) в запросе, например "в течение 10", для опроса каждые 10 секунд. Дополнительные сведения см. [в разделе предложение внутри](within-clause.md).

5.  Вызовите [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) с помощью запроса.

6.  Перебрать полученную коллекцию.

В следующем примере показано, как отслеживать вставку и удаление дисков с дисковода гибких дисков на локальном компьютере. Сценарий запрашивает \_ экземпляры [**\_ \_ инстанцемодификатионевент**](--instancemodificationevent.md) для экземпляра [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) на гибком диске и опрашивает их каждые 10 секунд для новых экземпляров. Этот сценарий является примером временного потребителя событий и продолжит выполнение до тех пор, пока оно не будет остановлено в диспетчере задач, или система не будет перезагружена. Дополнительные сведения см. [в статье получение событий в](receiving-events-for-the-duration-of-your-application.md)течение всего приложения.


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



В следующей процедуре описывается получение уведомления о событии семисинчронаус с помощью C++.

**Получение уведомления о событии семисинчронаус в C++**

1.  Настройте приложение с помощью вызовов функций [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    Поскольку WMI основан на COM, вызов [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) является обязательным шагом для приложения WMI. Дополнительные сведения см. [в разделе Создание приложения WMI или скрипта](creating-a-wmi-application-or-script.md).

2.  Определите тип событий, которые требуется получить.

    Инструментарий WMI поддерживает внутренние и внешние события. Внутреннее событие — это событие, предопределенное WMI. Внешнее событие является событием, определенным сторонним поставщиком. Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).

3.  Зарегистрируйтесь, чтобы получить конкретный класс событий с помощью вызова метода [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .

    Сделайте каждый запрос особым. Целью регистрации является регистрация для получения только необходимых уведомлений. Уведомления, не требующие траты времени на обработку и доставку.

    Потребитель событий можно спроектировать для получения нескольких событий. Например, потребителю может потребоваться уведомление о событиях изменения экземпляра для определенного класса событий нарушения безопасности. В этом случае задачи, выполняемые потребителем при получении события изменения экземпляра, отличаются для двух событий. Таким образом, потребитель должен выполнить один вызов [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) , чтобы зарегистрировать события изменения экземпляра, и еще один вызов **ексекнотификатионкуери** для регистрации событий нарушения безопасности.

    В вызове [**ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)задайте для параметра *лфлагс* значение, чтобы **\_ флаг WBEM \_ возвращался \_ немедленно** , а **флаг WBEM — \_ \_ \_ только вперед**. **Флаг WBEM \_ \_ возвращает \_** запросы, Семисинчронаус обработку, и флаг WBEM, показывающий **\_ \_ \_ только** однонаправленный перечислитель. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md). Функция **ексекнотификатионкуери** возвращает указатель на интерфейс [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

4.  Опрос для зарегистрированных уведомлений о событиях путем многократного вызова метода [**иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .
5.  По завершении выпустите перечислитель, указывающий на объект [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

    Вы можете освободить указатель [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , связанный с регистрацией. Освобождение указателя **IWbemServices** приводит к тому, что инструментарий WMI прекращает доставку событий всем связанным временным потребителям.

 

 
