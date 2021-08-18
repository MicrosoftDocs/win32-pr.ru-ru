---
title: Типы поддержки IAccessible
description: Типы поддержки IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb38ed0b5f7a306f2551085c77f77a3793efec3bc9281cd44d1d7277abe81fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993984"
---
# <a name="types-of-iaccessible-support"></a>Типы поддержки IAccessible

Серверы Microsoft Active Accessibility поддерживают два типа поддержки [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : Native и прокси. Элементы пользовательского интерфейса, используемые в приложении, определяют, какой тип поддержки подходит. Многие серверы, написанные сегодня, используют все преимущества прокси-серверов **IAccessible** и реализуют **IAccessible** для тех элементов управления, которые не являются Oleacc.dll, например безоконные элементы управления и элементы управления с настраиваемым именем класса окна.

## <a name="in-this-section"></a>Содержание раздела

-   [Реализация собственного Active Accessibility](native-active-accessibility-implementation.md)
-   [Прокси-серверы IAccessible](iaccessible-proxies.md)

 

 




