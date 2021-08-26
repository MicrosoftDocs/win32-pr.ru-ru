---
title: Сообщение PSM_INDEXTOID (Пршт. h)
description: Принимает индекс страницы свойств и возвращает идентификатор ресурса. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ индекстоид.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- элементы управления Windows сообщений PSM_INDEXTOID
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7a26cd97d324ae9bb4cfee85df00387c59293c7de8817b67da5605a207f07f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985724"
---
# <a name="psm_indextoid-message"></a>\_Сообщение ПСМ индекстоид

Принимает индекс страницы свойств и возвращает идентификатор ресурса. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ индекстоид**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс страницы.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает идентификатор ресурса страницы свойств, указанной параметром *wParam* в случае успеха. В противном случае возвращается ноль.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





