---
title: Сообщение TCM_GETCURSEL (Коммктрл. h)
description: Определяет текущую выбранную вкладку в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- элементы управления Windows сообщений TCM_GETCURSEL
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
ms.openlocfilehash: 6555194972467486789296377b5aaf87ca5520846ec9bf4c03ec345f635b6557
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104904"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





