---
description: '\_Константы побитового флага фонестатусфлагс описывают различные сведения о состоянии телефонного устройства.'
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Константы PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b42f8e13adfae54c56e44244d04b3961216edb87e29730fec6f689f315380a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060652"
---
# <a name="phonestatusflags_-constants"></a>\_Константы фонестатусфлагс

Константы побитового флага **фонестатусфлагс \_** описывают различные сведения о состоянии телефонного устройства.

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**ФОНЕСТАТУСФЛАГС \_ подключен**
</dt> <dd> <dl> <dt>



Указывает, подключен ли телефон к TAPI в данный момент. **Значение true** , если соединение установлено; в противном случае — **false** .


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**ФОНЕСТАТУСФЛАГС \_ приостановлен**
</dt> <dd> <dl> <dt>



Указывает, приостановлена ли работа TAPI телефонного устройства. **Значение true** , если suspended, и **false** в противном случае. Использование приложения телефонного устройства может быть временно приостановлено, когда коммутатор хочет управлять телефонным способом, который не допускает помех от приложения.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




