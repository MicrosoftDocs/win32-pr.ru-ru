---
title: Маска касания
description: Значения, которые могут отображаться в поле Таучмаск структуры POINTER_TOUCH_INFO.
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492645"
---
# <a name="touch-mask"></a>Маска касания

Значения, которые могут отображаться в поле **таучмаск** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .

<dl> <dt>

<span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE** 
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



По умолчанию. Все необязательные поля являются недопустимыми.


</dt> </dl> </dd> <dt>

<span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



**ркконтакт** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) является допустимой.


</dt> </dl> </dd> <dt>

<span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



допустима **ориентация** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .


</dt> </dl> </dd> <dt>

<span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



неправильное **давление** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





