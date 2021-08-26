---
description: '\_ \_ Константы поддержки конечных точек \_ xxx — это флаги поддержки оборудования для устройства конечной точки аудио.'
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Константы ENDPOINT_HARDWARE_SUPPORT_XXX (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c975a7bc00229943bb943035bf1fc84609414d83015ce4ae7d84d175b2e18a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053724"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>\_ \_ Константы поддержки конечных устройств \_ xxx

\_ \_ Константы поддержки конечных точек \_ xxx — это флаги поддержки оборудования для устройства конечной точки аудио.



| Константа/значение                                                                                                                                                                                                                                                                           | Описание                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**Конечная точка \_ \_ \_ Том аппаратной поддержки**</dt> <dt>0x00000001</dt> </dl> | Устройство конечной точки аудио поддерживает аппаратный регулятор громкости.<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**Конечная точка \_ АППАРАТная \_ поддержка не \_ поддерживает**</dt> <dt>0x00000002</dt> </dl>       | Устройство конечной точки аудио поддерживает аппаратный контроль звука.<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**Конечная точка \_ \_ \_ Счетчик аппаратной поддержки**</dt> <dt>0x00000004</dt> </dl>    | Устройство конечной точки аудио поддерживает счетчик пикового использования оборудования.<br/>     |



## <a name="remarks"></a>Remarks

Методы [**иаудиоендпоинтволуме:: куерихардваресуппорт**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) и [**Иаудиометеринформатион:: куерихардваресуппорт**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) используют \_ \_ константы поддержки конечных устройств \_ xxx.

Маска поддержки оборудования указывает, какие функции устройство аудио конечная точка реализует в оборудовании. Маска может быть либо 0, либо битовой или одной или несколькими \_ \_ константами поддержки конечных точек \_ xxx. Если в маске задан бит, соответствующий определенной \_ поддержке конечной точки \_ \_ xxx Constant, то это означает, что функция, представленная этой константой, реализована на устройстве оборудованием.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Ммдевицеапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Константы аудиоподсистемы Core](core-audio-constants.md)
</dt> <dt>

[**Иаудиоендпоинтволуме:: Куерихардваресуппорт**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**Иаудиометеринформатион:: Куерихардваресуппорт**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




