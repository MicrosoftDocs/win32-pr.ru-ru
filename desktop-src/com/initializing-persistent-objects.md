---
title: Инициализация постоянных объектов
description: Инициализация постоянных объектов
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549200"
---
# <a name="initializing-persistent-objects"></a>Инициализация постоянных объектов

Несколько постоянных интерфейсов объектов, [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [иперсистмемори](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))и [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), позволяют клиентам инициализировать объекты в состоянии "новое" или "по умолчанию". Это начальное состояние отличается от вновь созданного объекта, который не имеет состояния.

Инициализация состояния объекта даже до состояния по умолчанию может быть операцией ресурсоемких вычислений или ресурсов. Разделив создание на основе инициализации, инициализацию можно выполнить только в том случае, если она действительно необходима, и клиенты могут избежать инициализации объектов до состояния по умолчанию только для немедленной загрузки ранее сохраненных данных.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Постоянные интерфейсы объектов](persistent-object-interfaces.md)
</dt> </dl>

 

 