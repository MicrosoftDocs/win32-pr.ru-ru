---
title: Сообщение TCM_SETITEM (Коммктрл. h)
description: Задает некоторые или все атрибуты вкладки. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетитем.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- Элементы управления Windows для TCM_SETITEM сообщений
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801066"
---
# <a name="tcm_setitem-message"></a>\_Сообщение СЕТИТЕМ TCM

Задает некоторые или все атрибуты вкладки. Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетитем**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тЦитем**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , содержащую новые атрибуты элемента. Элемент **маски** указывает, какие атрибуты задаются. Если элемент **Mask** задает \_ текстовое значение тЦиф, то элемент **псзтекст** является адресом строки, завершающейся нулем, а элемент **кчтекстмакс** игнорируется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **TCM \_ СЕТИТЕМВ** (Юникод) и **TCM \_ сетитема** (ANSI)<br/>                   |



 

 





