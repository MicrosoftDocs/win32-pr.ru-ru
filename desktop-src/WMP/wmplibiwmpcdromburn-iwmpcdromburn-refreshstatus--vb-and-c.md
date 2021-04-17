---
title: Ивмпкдромбурн Рефрешстатус, метод
description: Метод Рефрешстатус обновляет сведения о состоянии текущего списка воспроизведения записи.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- Рефрешстатус метод Windows Media Player
- Рефрешстатус метод проигрывателя Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод Рефрешстатус
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717977"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a>Метод Ивмпкдромбурн:: Рефрешстатус

Метод **рефрешстатус** обновляет сведения о состоянии текущего списка воспроизведения записи.

## <a name="syntax"></a>Синтаксис


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод следует вызывать после создания или изменения списка воспроизведения записи перед чтением сведений о состоянии или записи компакт-диска. Чтобы проверить, требуется ли обновление, получите значение **бурнстате** и проверьте наличие вмпбсрефрешстатуспендинг.

Обновление состояния — это синхронная операция. Это означает, что длительный период времени может пройти, прежде чем этот метод возвратит значение, если текущий список воспроизведения имеет большой размер и содержит много изменений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромбурн. Бурнстате (VB и C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**вмпбурнстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





