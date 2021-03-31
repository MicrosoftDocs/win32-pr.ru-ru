---
title: Сообщение TCM_SETIMAGELIST (Коммктрл. h)
description: Присваивает список изображений элементу управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетимажелист.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- Элементы управления Windows для TCM_SETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071102"
---
# <a name="tcm_setimagelist-message"></a>\_Сообщение СЕТИМАЖЕЛИСТ TCM

Присваивает список изображений элементу управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетимажелист**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Обработчик для списка изображений, присваиваемый элементу управления "Вкладка".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на предыдущий список изображений или **значение NULL** , если предыдущий список изображений отсутствует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





