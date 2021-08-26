---
title: Сообщение TB_GETMAXSIZE (Коммктрл. h)
description: Возвращает общий размер всех видимых кнопок и разделителей на панели инструментов.
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- элементы управления Windows сообщений TB_GETMAXSIZE
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511d5726f117bbda183f55af5570fb75c2df3c78f5f6132dcefb406ee8fa7b70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918684"
---
# <a name="tb_getmaxsize-message"></a>\_Сообщение ЖЕТМАКССИЗЕ ТБ

Возвращает общий размер всех видимых кнопок и разделителей на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) , которая получает размер элементов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

