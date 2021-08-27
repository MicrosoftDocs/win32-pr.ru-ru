---
title: Сообщение PSM_IDTOINDEX (Пршт. h)
description: Принимает идентификатор ресурса страницы свойств и возвращает индекс, начинающийся с нуля. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ идтоиндекс.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- элементы управления Windows сообщений PSM_IDTOINDEX
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83bce0bfeecd2f233b2108133b08e49c27c90625c1bd07f2d4273bd77bbd0b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061524"
---
# <a name="psm_idtoindex-message"></a>\_Сообщение ПСМ идтоиндекс

Принимает идентификатор ресурса страницы свойств и возвращает индекс, начинающийся с нуля. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ идтоиндекс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Идентификатор ресурса страницы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает отсчитываемый от нуля индекс страницы вкладки свойств, указанной параметром *lParam* в случае успеха. Иначе возвращается значение -1.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





