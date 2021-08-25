---
title: Сообщение TTM_GETTEXT (Коммктрл. h)
description: Извлекает сведения о средстве, которые поддерживает элемент управления ToolTip.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- элементы управления Windows сообщений TTM_GETTEXT
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9efe79105c705eba3dd25c124cf17ff0e4773618608bc7ef86ebbf3d0d9f715e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967894"
---
# <a name="ttm_gettext-message"></a>ТТМ \_ SMS

Извлекает сведения о средстве, которые поддерживает элемент управления ToolTip.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Число **тчарс**, включая завершающее **значение NULL**, для копирования в буфер, на который указывает **лпсзтекст**. </dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Задайте для элемента **кбсизе** этой структуры значение `sizeof(TOOLINFO)` перед отправкой этого сообщения. Задайте элементы **HWND** и **uId** , чтобы определить средство, для которого требуется получить сведения. Выделение буфера размера, указанного параметром *wParam*. Установите элемент **лпсзтекст** , чтобы он указывал на буфер для получения текста инструмента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТМ \_ ЖЕТТЕКСТВ** (Юникод) и **ТТМ \_ gettext** (ANSI)<br/>                   |



 

 





