---
title: Архитектура служба удаленного управления Windows
description: Архитектура служба удаленного управления Windows состоит из компонентов на клиентских и серверных компьютерах.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793039"
---
# <a name="windows-remote-management-architecture"></a>Архитектура служба удаленного управления Windows

Архитектура служба удаленного управления Windows состоит из компонентов на клиентских и серверных компьютерах. На следующем рисунке показаны компоненты на обоих компьютерах, как компоненты взаимодействуют с другими компонентами, и протокол, используемый для обмена данными между компьютерами.

![Архитектура WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a>Запрос клиента

Следующие компоненты WinRM находятся на компьютере, на котором работает сценарий, запрашивающий данные.

-   Приложение WinRM

    Это сценарий или средство командной строки **WinRM** , которое использует API скриптов WinRM для вызова данных запроса или выполнения методов. Дополнительные сведения см. в разделе [API сценариев WinRM](winrm-scripting-api.md).

-   WSMAuto.dll

    Уровень автоматизации, обеспечивающий поддержку сценариев.

-   WsmCL.dll

    Уровень API C в операционной системе.

-   API HTTP

    Для WinRM требуется поддержка транспорта HTTP и HTTPS.

## <a name="responding-server"></a>Отвечающий сервер

Следующие компоненты WinRM находятся на отвечающем компьютере.

-   API HTTP

    Для WinRM требуется поддержка транспорта HTTP и HTTPS.

-   WSMAuto.dll

    Уровень автоматизации, обеспечивающий поддержку сценариев.

-   WsmCL.dll

    Уровень API C в операционной системе.

-   WsmSvc.dll

    Служба [*прослушивателя*](windows-remote-management-glossary.md) WinRM.

-   WsmProv.dll

    Подсистема поставщика.

-   WsmRes.dll

    Файл ресурсов.

-   WsmWmiPl.dll

    [*Подключаемый модуль WMI*](windows-remote-management-glossary.md). Это позволяет получать данные WMI с помощью WinRM.

-   Драйвер IPMI и поставщик IPMI WMI

    Эти компоненты предоставляют все данные оборудования, запрашиваемые с помощью классов IPMI. Дополнительные сведения см. в разделе [поставщик IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). Оборудование BMC должно быть обнаружено SMBIOS или устройством, созданным вручную путем загрузки драйвера. Дополнительные сведения см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> </dl>

 

 