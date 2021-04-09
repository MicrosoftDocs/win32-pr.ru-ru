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
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143183"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types. h (включение D3d9. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления видео Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




