---
title: Сообщение TCM_GETROWCOUNT (Коммктрл. h)
description: Извлекает текущее число строк вкладок в элементе управления "Вкладка". Это сообщение можно отправить явно или с помощью \_ макроса табктрл.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- Элементы управления Windows для TCM_GETROWCOUNT сообщений
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892530"
---
# <a name="tcm_getrowcount-message"></a>\_Сообщение TCM ROWCOUNT

Извлекает текущее число строк вкладок в элементе управления "Вкладка". Это сообщение можно отправить явно или с помощью макроса [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число строк вкладок.

## <a name="remarks"></a>Комментарии

Только элементы управления "Вкладка", имеющие [**\_ Многострочный стиль TCS**](tab-control-styles.md) , могут содержать несколько строк вкладок.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





