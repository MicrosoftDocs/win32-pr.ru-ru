---
title: Сообщение TCM_GETROWCOUNT (Коммктрл. h)
description: Извлекает текущее число строк вкладок в элементе управления "Вкладка". Это сообщение можно отправить явно или с помощью \_ макроса табктрл.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- элементы управления Windows сообщений TCM_GETROWCOUNT
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
ms.openlocfilehash: 9e67b2ac40834075b31ccf2415a52c96448b8143dde3d6bc67f9c515e1f601a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104874"
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

## <a name="remarks"></a>Remarks

Только элементы управления "Вкладка", имеющие [**\_ Многострочный стиль TCS**](tab-control-styles.md) , могут содержать несколько строк вкладок.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





