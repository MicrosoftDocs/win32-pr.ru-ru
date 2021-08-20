---
title: Сообщение MCM_GETCALENDARGRIDINFO (Коммктрл. h)
description: Возвращает сведения о сетке календаря.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- элементы управления Windows сообщений MCM_GETCALENDARGRIDINFO
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
ms.openlocfilehash: 26365b940b17617b1f00b93697fc78fa759dd2599d3398ccb8d92725159a70cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170171"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





