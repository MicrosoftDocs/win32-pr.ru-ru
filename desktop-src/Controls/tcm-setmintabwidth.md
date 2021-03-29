---
title: Сообщение TCM_SETMINTABWIDTH (Коммктрл. h)
description: Устанавливает минимальную ширину элементов в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетминтабвидс.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- Элементы управления Windows для TCM_SETMINTABWIDTH сообщений
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654414"
---
# <a name="tcm_setmintabwidth-message"></a>\_Сообщение СЕТМИНТАБВИДС TCM

Устанавливает минимальную ширину элементов в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетминтабвидс**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Минимальная ширина, устанавливаемая для элемента управления вкладки. Если этот параметр имеет значение-1, то элемент управления будет использовать ширину табуляции по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа INT, представляющее предыдущую минимальную ширину табуляции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





