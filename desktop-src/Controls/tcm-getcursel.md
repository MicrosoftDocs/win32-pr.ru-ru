---
title: Сообщение TCM_GETCURSEL (Коммктрл. h)
description: Определяет текущую выбранную вкладку в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- Элементы управления Windows для TCM_GETCURSEL сообщений
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654670"
---
# <a name="tcm_getcursel-message"></a>\_Сообщение TCM

Определяет текущую выбранную вкладку в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс выбранной вкладки, если она выполнена успешно, или значение-1, если вкладка не выбрана.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





