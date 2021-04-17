---
description: Константы побитового флага ФОНЕЛАМПМОДЕ описывают различные способы освещения лампы для телефонов.
ms.assetid: 4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe
title: Константы PHONELAMPMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8df5920df79e6fc59eb12bf1f517b4070e617d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680102"
---
# <a name="phonelampmode_-constants"></a>Константы PHONELAMPMODE_

**PHONELAMPMODE_** константы битовых флагов описывают различные способы освещения лампы телефона.

<dl> <dt>

<span id="PHONELAMPMODE_DUMMY"></span><span id="phonelampmode_dummy"></span>**PHONELAMPMODE_DUMMY**
</dt> <dd> <dl> <dt>



Это значение используется для описания расположения кнопки или лампы, не имеющей соответствующей лампы.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_BROKENFLUTTER"></span><span id="phonelampmode_brokenflutter"></span>**PHONELAMPMODE_BROKENFLUTTER**
</dt> <dd> <dl> <dt>



Неработающая флуттер — это геоположение Flash и флуттер.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLASH"></span><span id="phonelampmode_flash"></span>**PHONELAMPMODE_FLASH**
</dt> <dd> <dl> <dt>



Flash означает, что они замедляют включение и отключение.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLUTTER"></span><span id="phonelampmode_flutter"></span>**PHONELAMPMODE_FLUTTER**
</dt> <dd> <dl> <dt>



Флуттер означает быстрое включение и отключение.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_OFF"></span><span id="phonelampmode_off"></span>**PHONELAMPMODE_OFF**
</dt> <dd> <dl> <dt>



Лампа отключена.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_STEADY"></span><span id="phonelampmode_steady"></span>**PHONELAMPMODE_STEADY**
</dt> <dd> <dl> <dt>



Постоянное означает, что лампа постоянно горит.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_UNKNOWN"></span><span id="phonelampmode_unknown"></span>**PHONELAMPMODE_UNKNOWN**
</dt> <dd> <dl> <dt>



Режим лампы в настоящее время неизвестен.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_WINK"></span><span id="phonelampmode_wink"></span>**PHONELAMPMODE_WINK**
</dt> <dd> <dl> <dt>



Мультик означает нормальную скорость включения и отключения.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Старшие 16 бит можно назначить для расширений для конкретных устройств. 16 младших разрядов зарезервированы.

Когда точные и неравномерности ритмичности могут различаться для наборов телефонов разных поставщиков, сопоставление фактических шаблонов освещения для большинства телефонов со значениями, перечисленными выше, должно быть простым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




