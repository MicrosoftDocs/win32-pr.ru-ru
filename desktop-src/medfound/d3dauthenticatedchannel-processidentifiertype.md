---
description: Указывает тип процесса, определенного в \_ \_ выходной структуре D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесс.
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: Перечисление D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 522fee8421ec61b58bd67065c31b968252c2c7d563e94f7eda7a9f5105d20382
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061984"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a>\_Перечисление ПРОЦЕССИДЕНТИФИЕРТИПЕ D3DAUTHENTICATEDCHANNEL

Указывает тип процесса, определенного в [**\_ \_ выходной структуре D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесс**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**ПРОЦЕССИДТИПЕ \_ неизвестный**
</dt> <dd>

Неизвестный тип процесса.

</dd> <dt>

<span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**ПРОЦЕССИДТИПЕ \_ DWM**
</dt> <dd>

Процесс диспетчер окон рабочего стола (DWM).

</dd> <dt>

<span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**ПРОЦЕССИДТИПЕ, \_ обработчик**
</dt> <dd>

Обработка процесса.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>D3d9types. h (включение D3d9. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления видео Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




