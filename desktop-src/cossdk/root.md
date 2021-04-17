---
description: Содержит коллекции верхнего уровня в каталоге.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Корневая коллекция
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: ad896c69ab6fad75179c9bb30668143aa2ea741e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692008"
---
# <a name="root-collection"></a>Корневая коллекция

Содержит коллекции верхнего уровня в каталоге. Он не содержит ни одного объекта [**комадминкаталогобжект**](comadmincatalogobject.md) или не поддерживает какие бы то ни было свойства.

**Корневая** коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

Нельзя переходить к **корневой** коллекции из любой коллекции.

## <a name="members"></a>Элементы

**Корневая** коллекция наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Ниже перечислены коллекции верхнего уровня в каталоге.

-   [**аппликатионклустер**](applicationcluster.md)
-   [**аппликатионинстанцес**](applicationinstances.md)
-   [**Приложения**](applications.md)
-   [**компутерлист**](computerlist.md)
-   [**дкомпротоколс**](dcomprotocols.md)
-   [**евентклассесфориид**](eventclassesforiid.md)
-   [**филесфоримпорт**](filesforimport.md)
-   [**инпроксерверс**](inprocservers.md)
-   [**легацисерверс**](legacyservers.md)
-   [**локалкомпутер**](localcomputer.md)
-   [**Секции**](partitions.md)
-   [**партитионусерс**](partitionusers.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)
-   [**трансиентсубскриптионс**](transientsubscriptions.md)
-   [**вовинпроксерверс**](wowinprocservers.md)
-   [**вовлегацисерверс**](wowlegacyservers.md)

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
