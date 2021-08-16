---
title: Windows Архитектура удаленного управления
description: архитектура служба удаленного управления Windows состоит из компонентов на клиентских и серверных компьютерах.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 889a823c4c67bed29f9ce695d84c893654b541aed76e0c79860e31f24c543662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121602"
---
# <a name="windows-remote-management-architecture"></a>Windows Архитектура удаленного управления

архитектура служба удаленного управления Windows состоит из компонентов на клиентских и серверных компьютерах. На следующем рисунке показаны компоненты на обоих компьютерах, как компоненты взаимодействуют с другими компонентами, и протокол, используемый для обмена данными между компьютерами.

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

    Эти компоненты предоставляют все данные оборудования, запрашиваемые с помощью классов IPMI. Дополнительные сведения см. в разделе [поставщик IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). Оборудование BMC должно быть обнаружено SMBIOS или устройством, созданным вручную путем загрузки драйвера. дополнительные сведения см. в разделе [установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[о служба удаленного управления Windows](about-windows-remote-management.md)
</dt> </dl>

 

 