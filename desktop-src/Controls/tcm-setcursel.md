---
title: Сообщение TCM_SETCURSEL (Коммктрл. h)
description: Выбирает вкладку в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сеткурсел.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- элементы управления Windows сообщений TCM_SETCURSEL
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdfd0861f5249a823d9406b437fd0efbca64a757a4bcadd7991155a87ddbc59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104854"
---
# <a name="tcm_setcursel-message"></a>\_Сообщение СЕТКУРСЕЛ TCM

Выбирает вкладку в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сеткурсел**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс выбираемой вкладки.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс ранее выбранной вкладки в случае успеха, или-1 в противном случае.

## <a name="remarks"></a>Remarks

Элемент управления "Вкладка" не отправляет код уведомления [ТКН \_ Селчангинг](tcn-selchanging.md) или [ТКН \_ селчанже](tcn-selchange.md) , когда вкладка выбрана с помощью этого сообщения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





