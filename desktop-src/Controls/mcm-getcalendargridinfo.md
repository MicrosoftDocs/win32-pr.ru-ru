---
title: Сообщение MCM_GETCALENDARGRIDINFO (Коммктрл. h)
description: Возвращает сведения о сетке календаря.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- Элементы управления Windows для MCM_GETCALENDARGRIDINFO сообщений
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804145"
---
# <a name="mcm_getcalendargridinfo-message"></a>\_Сообщение MCM жеткалендаргридинфо

Возвращает сведения о сетке календаря.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**мкгридинфо**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) , содержащую сведения о сетке календаря.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Значение true** , если выполнено успешно; в противном случае — **false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





