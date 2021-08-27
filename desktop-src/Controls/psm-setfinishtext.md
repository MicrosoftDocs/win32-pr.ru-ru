---
title: Сообщение PSM_SETFINISHTEXT (Пршт. h)
description: Задает текст кнопки "Готово" в мастере, показывает и включает кнопку, а также скрывает кнопки "Далее" и "назад". Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сетфиништекст.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- элементы управления Windows сообщений PSM_SETFINISHTEXT
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a08cafbeafeccb2235cb9b653f997aa8c60bd5fd21a3ccbc92e572fa5d3d0db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088564"
---
# <a name="psm_setfinishtext-message"></a>\_Сообщение ПСМ сетфиништекст

Задает текст кнопки **"Готово"** в мастере, показывает и включает кнопку, а также скрывает кнопки " **Далее** " и " **назад** ". Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сетфиништекст**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на новый текст для кнопки **"Готово"** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

По умолчанию кнопка **"Готово"** не имеет сочетания клавиш. Вы можете создать сочетание клавиш с помощью этого сообщения, включив амперсанд (&) в текстовую строку, назначенную для *lParam*. Например, "&Finish" определяет F в качестве сочетания клавиш.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ПСМ \_ СЕТФИНИШТЕКСТВ** (Юникод) и **ПСМ \_ сетфиништекста** (ANSI)<br/>    |



 

 





