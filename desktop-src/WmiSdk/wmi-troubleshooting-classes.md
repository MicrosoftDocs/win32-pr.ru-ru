---
description: Инструментарий WMI предоставляет набор классов для устранения неполадок, которые сценарии и приложения могут использовать для получения сведений о внутреннем состоянии WMI во время операций WMI Core и provider.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Классы устранения неполадок WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999555"
---
# <a name="wmi-troubleshooting-classes"></a>Классы устранения неполадок WMI

Инструментарий WMI предоставляет набор классов для устранения неполадок, которые сценарии и приложения могут использовать для получения сведений о внутреннем состоянии WMI во время операций WMI Core и provider. Дополнительные сведения об устранении неполадок WMI см. в разделе [Устранение неполадок WMI](wmi-troubleshooting.md) и [Настройка поставщика и устранение неполадок](provider-configuration-and-troubleshooting-classes.md).

Инструментарий WMI имеет несколько основных классов устранения неполадок для WMI Core и операций поставщика:

-   [**\_ \_ Счетчики MSFT события**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    На каждой системе компьютера обнаружен только один из этих классов. Он предоставляет счетчики различных операций поставщика в этой системе.

-   [**MSFT \_ вмиселфевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    Классы устранения неполадок событий являются производными от [**MSFT \_ вмиселфевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent). Запросы этого класса возвращают экземпляры классов событий, таких как [**MSFT \_ Вмисреадпулкреатед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) или [**MSFT \_ события \_ креатеинстанцеенумасинцевент \_ POST**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).

    В следующем списке приведены ссылки на различные категории классов событий, производных от [**MSFT \_ вмиселфевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):

    -   [Классы устранения неполадок событий поставщика](provider-event-troubleshooting-classes.md)
    -   [Классы устранения неполадок Консумерпровидер](consumerprovider-troubleshooting-classes.md)
    -   [Классы устранения неполадок событий службы WMI](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устранение неполадок WMI](wmi-troubleshooting.md).
</dt> <dt>

[Получение события WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
