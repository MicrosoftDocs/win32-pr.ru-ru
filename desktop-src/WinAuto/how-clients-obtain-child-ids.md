---
title: Получение идентификаторов дочерних объектов клиентами
description: Получение идентификаторов дочерних объектов клиентами
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a12dc3f40c2aaa776c1fa8e61713c52ffbdcde554c9f6a1cbca7093998780c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388604"
---
# <a name="how-clients-obtain-child-ids"></a>Получение идентификаторов дочерних объектов клиентами

Разработчики клиента могут получить идентификатор дочернего объекта следующим образом:

-   Вызовите [**акцессиблечилдрен**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren). Эта функция получает массив [**вариативных**](variant-structure.md) структур.
-   Запросите объект, чтобы узнать, поддерживает ли он интерфейс [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) . Если он имеется, используйте [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) , чтобы получить идентификаторы дочерних элементов.
-   Собирайте идентификаторы дочерних элементов, вызвав метод [**IAccessible:: аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) родительского объекта.

> [!Note]  
> Клиент обязан освободить память, используемую для структур [**вариантов**](variant-structure.md) . Клиенты также должны вызывать метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) для любого возвращаемого интерфейса [**IDispatch**](idispatch-interface.md) .

 

 

 