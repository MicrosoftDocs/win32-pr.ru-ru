---
title: Сообщение LVM_ARRANGE (Коммктрл. h)
description: Упорядочивает элементы в представлении значков. Это сообщение можно отправить явно или с помощью \_ макроса компоновки ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- Элементы управления Windows для LVM_ARRANGE сообщений
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
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135143"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





