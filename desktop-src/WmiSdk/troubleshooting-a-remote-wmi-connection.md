---
description: В следующих разделах описываются распространенные проблемы, с которыми могут столкнуться разработчики при создании удаленного WMI-подключения.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Устранение неполадок удаленного WMI-подключения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692691"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Устранение неполадок удаленного WMI-подключения

В следующих разделах описываются распространенные проблемы, с которыми могут столкнуться разработчики при создании удаленного WMI-подключения.

В этом разделе обсуждаются следующие разделы:

-   [Отказано в доступе DCOM](#dcom-access-denied)
-   [Не удалось подключиться](#failure-to-connect)
-   [Истекло время ожидания подключения WMI](#wmi-connection-timed-out)
-   [См. также](#related-topics)

## <a name="dcom-access-denied"></a>Отказано в доступе DCOM

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Случай
</dt> <dd>

произошел сбой подключения с ошибкой "DCOM-доступ запрещен", а также десятичное значение-2147024891 или шестнадцатеричный value0x80070005.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue
</dt> <dd>

Невозможно настроить DCOM для разрешения WMI-подключения.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Разрешением
</dt> <dd>

Параметры DCOM для WMI можно настроить с помощью служебной программы настройки DCOM (**DCOMCnfg.exe**), которая находится в **меню "Администрирование** " на **панели управления**. Эта программа предоставляет параметры, позволяющие определенным пользователям подключаться к компьютеру удаленно через DCOM. Члены группы "Администраторы" могут удаленно подключаться к компьютеру по умолчанию. С помощью этой служебной программы можно настроить безопасность для запуска, доступа и настройки службы WMI.

Дополнительные сведения см. [в разделе Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md).

</dd> </dl>

## <a name="failure-to-connect"></a>Не удалось подключиться

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Случай
</dt> <dd>

Невозможно подключиться к инструментарию WMI в удаленной системе.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue
</dt> <dd>

Возможно, вы пытаетесь подключиться к системе, которая не поддерживает Инструментарий WMI. Следующие подключения между версиями операционной системы не поддерживаются:

-   Невозможно подключиться к компьютеру, на котором выполняется начальное, базовое или Домашняя версии.

Кроме того, возможно, вы пытаетесь подключиться к пространству имен, для которого требуется зашифрованное соединение, которое требует уровня проверки подлинности `pktPrivacy` , **Вбемаусентикатионлевелпктприваци** или **RPC \_ C \_ AUTHN на \_ уровне \_ \_ безопасности PKT**.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Разрешением
</dt> <dd>

Дополнительные сведения см. в статьях [Защита пространств имен WMI](securing-wmi-namespaces.md), [Защита клиентов и поставщиков C++](securing-c---clients-and-providers.md)или [Установка уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>Истекло время ожидания подключения WMI

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Случай
</dt> <dd>

Истекло время ожидания подключения WMI.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue
</dt> <dd>

Из-за проблем с задержкой сети компьютер просто не может ответить вовремя.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Разрешением
</dt> <dd>

При подключении к инструментарию WMI с помощью вызова [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) или [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)можно задать флаг **вбемконнектфлагусемаксваит** (скрипт) или установить **\_ флаг WBEM \_ Connect \_ использовать максимальное время \_ \_ ожидания** в C++ значение 128 (0x80), чтобы наложить в вызове два (2) минуты.

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



