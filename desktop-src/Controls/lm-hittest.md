---
title: Сообщение LM_HITTEST (Коммктрл. h)
description: Определяет, щелкнул ли пользователь указанную ссылку.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- Элементы управления Windows для LM_HITTEST сообщений
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
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891453"
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

## <a name="remarks"></a>Комментарии

Если сообщение **\_ HITTEST LM** выполняется, система заполняет [**Литем. ILink**](/windows/win32/api/commctrl/ns-commctrl-litem) и **литем. сзид**. Если сообщение **\_ HITTEST LM** не выполняется, не считайте, что любая информация в **литем** является допустимой.

> [!Note]  
> Чтобы использовать этот API, необходимо предоставить манифест, задающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





