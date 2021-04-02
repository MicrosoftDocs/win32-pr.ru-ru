---
title: Управление дескрипторами
description: Диспетчер таблиц маршрутизации поддерживает подсчет ссылок для всех поддерживаемых сведений.
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24653dd98db9b0427e5a3bee3f2f6613a68ce41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986570"
---
# <a name="managing-handles"></a>Управление дескрипторами

Диспетчер таблиц маршрутизации поддерживает подсчет ссылок для всех поддерживаемых сведений. Это не позволяет диспетчеру таблиц маршрутизации возвращать клиенту дескрипторы памяти, которые были освобождены. Каждый раз при возврате маркера в вызывающий объект либо в виде явного маркера, либо в составе информационной структуры, например в [**\_ \_ сведениях**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info)о назначении RTM, счетчик ссылок для объекта, соответствующего этому маркеру, увеличивается. При освобождении маркера или структуры информации соответствующий счетчик ссылок уменьшается. Когда число ссылок становится равным нулю, объект освобождается.

Функции [**ртмжетдестинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**ртмжетентитинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**ртмжетраутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) и [**ртмжетнекссопинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) возвращают структуры информации. Эти функции соответствуют функциям [**ртмрелеаседестинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**ртмрелеасинтитинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**ртмрелеасераутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) и [**ртмреласенекссопинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) соответственно.

> [!Note]  
> Функция [**ртмрелеасечанжеддестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) должна использоваться для освобождения дескрипторов, возвращенных вызовом [**ртмжетчанжеддестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests). Не используйте [**ртмрелеаседестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) для измененных целевых структур.

 

Если клиент должен сохранять конкретный маркер в информационной структуре при освобождении остальных, клиент может вызвать [**ртмреференцехандлес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) с этим обработчиком перед тем, как освободить информационную структуру. Затем этот маркер можно освободить с помощью вызова функций [**ртмрелеаседестинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**ртмрелеасинтитинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**ртмрелеасераутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) и [**ртмреласенекссопинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) .

 

 




