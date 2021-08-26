---
title: Сообщение LVM_ARRANGE (Коммктрл. h)
description: Упорядочивает элементы в представлении значков. Это сообщение можно отправить явно или с помощью \_ макроса компоновки ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- элементы управления Windows сообщений LVM_ARRANGE
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98d7e3595c276815af8708a54d6e81c2a40192d8d07e6cbce514481723799d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062654"
---
# <a name="lvm_arrange-message"></a>LVM \_ Размещение сообщения

Упорядочивает элементы в представлении значков. Это сообщение можно отправить явно или с помощью макроса [**\_ компоновки ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Одно из следующих значений, определяющее выравнивание:



| Значение                                                                                                                                                            | Значение                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**ЛВА \_ алигнлефт**</dt> </dl>    | Не реализован. Примените вместо этого стиль [**LVS \_ алигнлефт**](list-view-window-styles.md) .<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**ЛВА \_ алигнтоп**</dt> </dl>       | Не реализован. Примените вместо этого стиль [**LVS \_ алигнтоп**](list-view-window-styles.md) .<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**ЛВА \_ по умолчанию**</dt> </dl>          | Выравнивает элементы в соответствии с текущими стилями выравнивания элемента управления представления списка (значение по умолчанию).<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**ЛВА \_ SNAPTOGRID**</dt> </dl> | Привязывает все значки к ближайшей положению сетки.<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





