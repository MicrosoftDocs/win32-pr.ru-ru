---
title: Сообщение TTM_GETTEXT (Коммктрл. h)
description: Извлекает сведения о средстве, которые поддерживает элемент управления ToolTip.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- Элементы управления Windows для TTM_GETTEXT сообщений
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
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654502"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТМ \_ ЖЕТТЕКСТВ** (Юникод) и **ТТМ \_ gettext** (ANSI)<br/>                   |



 

 





