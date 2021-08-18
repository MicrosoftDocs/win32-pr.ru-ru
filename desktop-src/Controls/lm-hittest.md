---
title: Сообщение LM_HITTEST (Коммктрл. h)
description: Определяет, щелкнул ли пользователь указанную ссылку.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- элементы управления Windows сообщений LM_HITTEST
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 559ea1500c7270ece1785391777133bdaaeb1e95e5b01fa5ca7d4bb76e40f1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958382"
---
# <a name="lm_hittest-message"></a>\_Сообщение HITTEST LM

Определяет, щелкнул ли пользователь указанную ссылку.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен иметь **значение NULL**.</dd> <dt>

*lParam* 
</dt> <dd>Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**лхиттестинфо**</a> для заполнения данными о ссылке, которую щелкнул пользователь, если таковой имеется. </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если пользователь щелкнул ссылку; в противном случае возвращает **значение false**.

## <a name="remarks"></a>Remarks

Если сообщение **\_ HITTEST LM** выполняется, система заполняет [**Литем. ILink**](/windows/win32/api/commctrl/ns-commctrl-litem) и **литем. сзид**. Если сообщение **\_ HITTEST LM** не выполняется, не считайте, что любая информация в **литем** является допустимой.

> [!Note]  
> Чтобы использовать этот API, необходимо предоставить манифест, задающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





