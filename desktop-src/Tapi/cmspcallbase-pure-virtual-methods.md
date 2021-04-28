---
description: Кмспкаллбасе чистые виртуальные методы. Эти методы должны быть переопределены производными классами.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Чистые виртуальные методы Кмспкаллбасе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094462"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>Чистые виртуальные методы Кмспкаллбасе

Эти методы должны быть переопределены производными классами.



| Чистые виртуальные методы Кмспкаллбасе                                 | Описание                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**мспкалладдреф**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Закрытый метод AddRef для объекта вызова.                                                                                              |
| [**мспкаллрелеасе**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Частный метод освобождения для объекта Call.                                                                                             |
| [**Ini**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Вызывается объектом-адресом MSP (в методе [**креатемспкалл**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) для инициализации объекта вызова MSP. |
| [**Закрытия**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Вызывается объектом адреса MSP для завершения вызова..                                                                                |
| [**интерналкреатестреам**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Вызывается методом [**креатестреам**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) для создания объекта потока.                                               |
| [**креатестреамобжект**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | Вызывается методом [**интерналкреатестреам**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) для создания объекта потока.                                  |
| [**ремовестреам**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | Вызывается приложением для удаления потока из вызова                                                                              |



 

## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[**кмспкаллбасе**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
