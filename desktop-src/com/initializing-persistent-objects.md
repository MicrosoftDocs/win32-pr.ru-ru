---
title: Инициализация постоянных объектов
description: Инициализация постоянных объектов
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211d9d89b7a8f36ab06d9930e45f365e0fb5d4dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413817"
---
# <a name="initializing-persistent-objects"></a>Инициализация постоянных объектов

Несколько постоянных интерфейсов объектов, [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [иперсистмемори](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))и [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), позволяют клиентам инициализировать объекты в состоянии "новое" или "по умолчанию". Это начальное состояние отличается от вновь созданного объекта, который не имеет состояния.

Инициализация состояния объекта даже до состояния по умолчанию может быть операцией ресурсоемких вычислений или ресурсов. Разделив создание на основе инициализации, инициализацию можно выполнить только в том случае, если она действительно необходима, и клиенты могут избежать инициализации объектов до состояния по умолчанию только для немедленной загрузки ранее сохраненных данных.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Постоянные интерфейсы объектов](persistent-object-interfaces.md)
</dt> </dl>

 

 