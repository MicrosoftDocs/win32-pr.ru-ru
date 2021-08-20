---
description: Кмспкаллбасе чистые виртуальные методы. Эти методы должны быть переопределены производными классами.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Чистые виртуальные методы Кмспкаллбасе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9fdd6fb66c0dd7dabfcf2b78866b49ff617cfca22a53495ad23b35680d7b47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947173"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>Чистые виртуальные методы Кмспкаллбасе

Эти методы должны быть переопределены производными классами.



| Чистые виртуальные методы Кмспкаллбасе                                 | Описание:                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**мспкалладдреф**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Закрытый метод AddRef для объекта вызова.                                                                                              |
| [**мспкаллрелеасе**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Частный метод освобождения для объекта Call.                                                                                             |
| [**Init**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Вызывается объектом-адресом MSP (в методе [**креатемспкалл**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) для инициализации объекта вызова MSP. |
| [**Закрытия**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Вызывается объектом адреса MSP для завершения вызова..                                                                                |
| [**интерналкреатестреам**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Вызывается методом [**креатестреам**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) для создания объекта потока.                                               |
| [**креатестреамобжект**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | Вызывается методом [**интерналкреатестреам**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) для создания объекта потока.                                  |
| [**ремовестреам**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | Вызывается приложением для удаления потока из вызова                                                                              |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**кмспкаллбасе**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
