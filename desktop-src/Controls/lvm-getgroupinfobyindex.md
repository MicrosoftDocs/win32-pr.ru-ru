---
title: Сообщение LVM_GETGROUPINFOBYINDEX (Коммктрл. h)
description: Возвращает сведения о указанной группе. Отправьте это сообщение явным образом или с помощью \_ макроса Жетграупинфобиндекс ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- Элементы управления Windows для LVM_GETGROUPINFOBYINDEX сообщений
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
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136418"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





