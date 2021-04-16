---
description: В следующей таблице перечислены классы событий для устранения неполадок, создаваемые операциями поставщика потребителей событий.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Классы устранения неполадок Консумерпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536c23fb35ca6a4d2146cf87782768c51f37a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712469"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Классы устранения неполадок Консумерпровидер

В следующей таблице перечислены классы событий для устранения неполадок, создаваемые операциями [*поставщика потребителей событий*](gloss-e.md) .

Вы можете подписываться на абстрактный базовый класс уведомлений [**MSFT \_ провидеревент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) , чтобы получить все следующие события.



|                                                                                                 |                                                                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSFT \_ вмипровидеревент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Родительский класс для всех событий поставщика потребителей.                                  |
| [**MSFT \_ вмиконсумерпровидерлоадед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Определяет успешную активацию COM-объекта поставщика событий потребителей.    |
| [**MSFT \_ вмиконсумерпровидерунлоадед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Определяет успешную деактивацию COM-объекта поставщика событий потребителей.  |
| [**MSFT \_ вмиконсумерпровидерсинклоадед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Определяет успешную активацию объекта приемника поставщика событий.   |
| [**MSFT \_ вмиконсумерпровидерсинкунлоадед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Определяет успешную деактивацию объекта приемника поставщика событий. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устранение неполадок WMI](wmi-troubleshooting.md).
</dt> <dt>

Устранение неполадок инструментария WMI
</dt> <dt>

[Получение события WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
