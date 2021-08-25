---
title: Сообщение TCM_SETPADDING (Коммктрл. h)
description: Задает объем пространства (заполнение) вокруг значка и метки каждой вкладки в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетпаддинг.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- элементы управления Windows сообщений TCM_SETPADDING
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969ae3c7c240c38a6643682321c14e5744f2d2c2eec188004d1c3b2e6f2b3835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876244"
---
# <a name="tcm_setpadding-message"></a>\_Сообщение СЕТПАДДИНГ TCM

Задает объем пространства (заполнение) вокруг значка и метки каждой вкладки в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетпаддинг**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это значение **типа int** , определяющее величину отступа по горизонтали (в пикселях). [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — это значение **типа int** , указывающее величину вертикального заполнения (в пикселях).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

