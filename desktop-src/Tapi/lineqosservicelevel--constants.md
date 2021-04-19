---
description: Эти константы используются TSP для выяснения типа требуемого уровня качества обслуживания (Quality Service).
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: Константы LINEQOSSERVICELEVEL_ (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689172"
---
# <a name="lineqosservicelevel_-constants"></a>\_Константы линекоссервицелевел

Эти константы используются TSP для выяснения типа требуемого уровня качества обслуживания (Quality Service).

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**\_требуется линекоссервицелевел**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Запрошенный уровень качества обслуживания является обязательным.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**ЛИНЕКОССЕРВИЦЕЛЕВЕЛ \_ ифаваилабле**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Требуемый уровень качества обслуживания, если он доступен.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**ЛИНЕКОССЕРВИЦЕЛЕВЕЛ \_ бестеффорт**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Требуемый уровень качества обслуживания — «лучшие усилия».


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>Тспи. h</dt> </dl> |



 

 




