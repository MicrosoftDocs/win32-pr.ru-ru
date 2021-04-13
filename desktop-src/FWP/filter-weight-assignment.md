---
title: Назначение весов фильтрам
description: Каждый фильтр в платформе фильтрации Windows (WFP) имеет соответствующий вес, который используется во время арбитража фильтра.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/26/2020
ms.locfileid: "104412711"
---
# <a name="filter-weight-assignment"></a>Назначение весов фильтрам

Каждый фильтр в платформе фильтрации Windows (WFP) имеет соответствующий вес, который используется во время [арбитража фильтра](filter-arbitration.md).

Вес фильтра, используемый модулем базовой фильтрации (BFE), имеет тип [**\_ UINT64 FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). При добавлении фильтров вызывающие объекты имеют три варианта.

-   Задайте вес в виде [**\_ UINT64 FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). В BFE используется указанный весовой коэффициент.
-   Задайте для параметра вес значение [**FWP \_ Empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). BFE автоматически создает вес в диапазоне от \[ 0 до 2 ⁶ ⁰).
-   Задайте вес [**FWP \_ UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) в диапазоне от \[ 0 до 15 \] . В BFE в качестве идентификатора диапазона веса используется указанный вес.

    BFE автоматически создает младшие биты 60 (точно так же, как если бы весовой коэффициент был установлен в [**FWP \_ Empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), а затем использует предоставленное значение для установки 4 старших битов. Это позволяет вызывающим объектам вручную разделить пространство веса на 16 диапазонов, при этом используя Автоматическое взвешивание в пределах диапазона.

> [!Note]  
> Если в одном подуровне зарегистрировано несколько вызовов, могут возникнуть проблемы, если фильтрам назначен один и тот же вес. Эту ошибку можно предотвратить, выполнив выноски, создав свой собственный подуровень с помощью [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Идентификаторы веса фильтра**](filter-weight-identifiers.md)
</dt> </dl>

 

 




