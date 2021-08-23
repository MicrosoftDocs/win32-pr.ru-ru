---
title: Сообщение SB_GETTIPTEXT (Коммктрл. h)
description: Извлекает текст подсказки для части в строке состояния. Чтобы включить подсказки, необходимо создать строку состояния с помощью \_ стиля подсказок SBT.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- элементы управления Windows сообщений SB_GETTIPTEXT
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a78fa6650d850cad2b6de8cc77f1d44b49b8325bf6856b989953fc6511f56f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637134"
---
# <a name="sb_gettiptext-message"></a>\_Сообщение SB жеттиптекст

Извлекает текст подсказки для части в строке состояния. Чтобы включить подсказки, необходимо создать строку состояния с помощью стиля [**\_ подсказок SBT**](status-bar-styles.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) Указывает отсчитываемый от нуля индекс части, которая получает текст подсказки. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает размер буфера в параметре *lParam* в символах.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на символьный буфер, который получает текст подсказки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Remarks

**Предупреждение системы безопасности:** Неправильное использование этого сообщения может привести к проблемам с приложением. Например, если текст слишком велик для буфера *lParam* , это может привести к переполнению буфера. прежде чем продолжить, ознакомьтесь с [вопросами безопасности: Microsoft Windows](sec-comctls.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **SB \_ ЖЕТТИПТЕКСТВ** (Юникод) и **SB \_ жеттиптекста** (ANSI)<br/>               |



 

