---
title: Оценки проверки попадания касания
description: Следующие константы указывают на возможные результаты проверки попадания для объекта относительно других объектов, пересекающих зону касания.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 18b321272637f4e6931bdc9115e64f8b0553e90e94d8013147ca7a577bad1eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758016"
---
# <a name="touch-hit-testing-scores"></a>Оценки проверки попадания касания

Следующие константы указывают на возможные результаты проверки попадания для объекта относительно других объектов, пересекающих зону касания.

| Константа/значение | Описание |
|---|---|
| **TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0      | Объект является наиболее вероятной целью.<br/>  |
| **TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xfff | Объект является наименее вероятной целью.<br/> |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Header<br/>                   | Winuser. h |
