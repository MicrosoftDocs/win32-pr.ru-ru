---
title: Извлечение сведений
description: RTMv2 позволяет клиенту получать информацию, на которую ссылается данный обработчик, с помощью функций Ртмжетентитинфо, Ртмжетдестинфо, Ртмжетраутеинфо и Ртмжетнекссопинфо.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51958fccc8a07e8846705945d9210f4259dfd89b1e3cefccd65d57dd0f033757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028024"
---
# <a name="retrieving-information"></a>Извлечение сведений

RTMv2 позволяет клиенту получать информацию, на которую ссылается данный обработчик, с помощью функций [**ртмжетентитинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**ртмжетдестинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**ртмжетраутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)и [**ртмжетнекссопинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .

Эти вызовы функций имеют соответствующие функции ([**ртмрелеасинтитинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**ртмрелеаседестинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**ртмрелеасераутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**ртмрелеасенекссопинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) для освобождения дескрипторов, связанных со структурой данных, возвращаемой диспетчером таблиц маршрутизации.

> [!Note]  
> Сведения для клиентов доступны только в текущем экземпляре и семействе адресов.

 

Пример кода, демонстрирующий использование этих функций, см. [в разделе Поиск лучшего маршрута](search-for-the-best-route.md).

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>Использование Ртмжетексактматчрауте и Ртмжетексактматчдестинатион

Функции [**ртмжетексактматчрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) и [**ртмжетексактматчдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) используются клиентами для поиска конкретного маршрута или назначения. Эти функции экономируют время, выполняя операции сравнения для клиента.

Например, когда RIP обновляет маршрут, RIP должен хранить старые сведения о метриках. RIP ищет маршрут и сведения о нем. Затем RIP может скопировать информацию и обновить маршрут.

## <a name="using-rtmgetmostspecificdestination"></a>Использование РтмжетмостспеЦификдестинатион

Функция [**ртмжетмостспеЦификдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) используется для поиска места назначения, которое лучше соответствует указанному сетевому префиксу.

Например, Диспетчер групп многоадресной рассылки использует эту функцию для выполнения проверки с обратным путем перенаправления (РПФ) на одном адресе. Функцию также можно использовать для поиска локального следующего прыжка для данного удаленного следующего прыжка.

Пример кода, демонстрирующий использование этих функций, см. в разделе [Поиск маршрутов с помощью дерева префиксов](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) и [Поиск лучшего маршрута](search-for-the-best-route.md).

## <a name="using-rtmgetlessspecificdestination"></a>Использование РтмжетлессспеЦификдестинатион

Функция [**ртмжетлессспеЦификдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) используется для поиска назначения, которое является наиболее подходящей для указанного префикса сети. Эту функцию можно вызвать многократно, чтобы вернуть следующее повторяющееся совпадение с меньшим соответствием, пока не будут найдены другие назначения.

Эта функция вызывается после вызова [**ртмжетмостспеЦификдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).

Пример кода, демонстрирующий использование этих функций, см. в разделе [Поиск маршрутов с помощью дерева префиксов](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).

## <a name="using-rtmisbestroute"></a>Использование Ртмисбестрауте

Функция [**ртмисбестрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) позволяет клиенту быстро определить, является ли конкретный маршрут лучшим маршрутом к назначению. Например, клиенту может потребоваться хранить определенный маршрут только в том случае, если это лучший маршрут. Таким образом, клиент может вызвать эту функцию вместо перечисления всех маршрутов и выполнения сравнения.

 

 




