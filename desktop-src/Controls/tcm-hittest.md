---
title: Сообщение TCM_HITTEST (Коммктрл. h)
description: Определяет, какая вкладка, если она есть, находится на заданной позиции экрана. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- Элементы управления Windows для TCM_HITTEST сообщений
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654666"
---
# <a name="tcm_hittest-message"></a>\_Сообщение HITTEST TCM

Определяет, какая вкладка, если она есть, находится на заданной позиции экрана. Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тчиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) , указывающую, на какой позиции экрана нужно выполнить проверку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс вкладки или значение-1, если вкладка не находится в указанной позиции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





