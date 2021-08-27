---
title: Сообщение TB_GETBITMAP (Коммктрл. h)
description: Извлекает индекс растрового изображения, связанного с кнопкой на панели инструментов.
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- элементы управления Windows сообщений TB_GETBITMAP
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb976d206de0cdbd0234763f92ac0417cc974355a3371d04476d7969e1f763c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957913"
---
# <a name="tb_getbitmap-message"></a>(ТБ) \_ сообщение с изображением

Извлекает индекс растрового изображения, связанного с кнопкой на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор команды для кнопки, индекс которой необходимо получить.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс битовой карты в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





