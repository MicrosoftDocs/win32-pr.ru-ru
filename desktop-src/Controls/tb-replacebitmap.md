---
title: Сообщение TB_REPLACEBITMAP (Коммктрл. h)
description: Заменяет существующий точечный рисунок новым растровым изображением.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- элементы управления Windows сообщений TB_REPLACEBITMAP
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11dd964691b8b854feb09f93bc03673c46103bb34842e326e0f433cfd1fcc77f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968054"
---
# <a name="tb_replacebitmap-message"></a>\_Сообщение РЕПЛАЦЕБИТМАП ТБ

Заменяет существующий точечный рисунок новым растровым изображением.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тбреплацебитмап**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) , которая содержит сведения о заменяемом растровом изображении, и новое растровое изображение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





