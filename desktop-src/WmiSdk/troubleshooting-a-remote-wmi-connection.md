---
description: В следующих разделах описываются распространенные проблемы, с которыми могут столкнуться разработчики при создании удаленного WMI-подключения.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Устранение неполадок удаленного WMI-подключения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10603f713fecf861750d70c4166da91e081dc273a0d6d6134ed916a7f84f2bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312420"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Устранение неполадок удаленного WMI-подключения

В следующих разделах описываются распространенные проблемы, с которыми могут столкнуться разработчики при создании удаленного WMI-подключения.

В этом разделе обсуждаются следующие разделы:

-   [Отказано в доступе DCOM](#dcom-access-denied)
-   [сбой Подключение](#failure-to-connect)
-   [Истекло время ожидания подключения WMI](#wmi-connection-timed-out)
-   [Связанные темы](#related-topics)

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

## <a name="failure-to-connect"></a>сбой Подключение

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



