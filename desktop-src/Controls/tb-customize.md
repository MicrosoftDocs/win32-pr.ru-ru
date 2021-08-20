---
title: Сообщение TB_CUSTOMIZE (Коммктрл. h)
description: Отображает диалоговое окно Настройка панели инструментов.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- элементы управления Windows сообщений TB_CUSTOMIZE
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c4fe1cba535903ff1e60804ee6d4ec5743f5d3726212f9aca16742a40913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957933"
---
# <a name="tb_customize-message"></a>\_Настраиваемое сообщение (ТБ)

Отображает диалоговое окно **Настройка панели инструментов** .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

> [!Note]  
> Панель инструментов должна поддерживать уведомления [ТБН \_ Куеринсерт](tbn-queryinsert.md) и [ТБН \_ куериделете](tbn-querydelete.md) для отображения диалогового окна **Настройка панели инструментов** . Если панель инструментов не обрабатывает эти уведомления, **\_ Настройка ТБ** не влияет.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





