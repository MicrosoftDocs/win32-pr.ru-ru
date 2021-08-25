---
title: Сообщение LVM_GETGROUPINFOBYINDEX (Коммктрл. h)
description: Возвращает сведения о указанной группе. Отправьте это сообщение явным образом или с помощью \_ макроса Жетграупинфобиндекс ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- элементы управления Windows сообщений LVM_GETGROUPINFOBYINDEX
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482683e9d1026c1deed17bf1f05310d63ac2127a6a2a6f32b5b5d95a0fbbea3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877404"
---
# <a name="lvm_getgroupinfobyindex-message"></a>\_Сообщение LVM жетграупинфобиндекс

Возвращает сведения о указанной группе. Отправьте это сообщение явным образом или с помощью макроса [**\_ жетграупинфобиндекс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Индекс группы.

</dd> <dt>

*lParam* \[ в, out\]
</dt> <dd>

Указатель на структуру [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) для получения сведений о группе, заданной параметром *wParam*. Вызывающий процесс отвечает за выделение памяти для структуры и всех буферов в структуре, например, на которую указывает элемент **псзеадер** . Задайте все элементы, которые являются производными структуры, например **кчхеадер** размер буфера, на который указывает **псзеадер** в **Вчарс** , включая завершающее **значение NULL**. Задайте для **кбсизе** значение sizeof (лвграуп).

Получатель сообщений отвечает за присвоение членам структуры сведений о группе, заданной параметром *wParam*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





