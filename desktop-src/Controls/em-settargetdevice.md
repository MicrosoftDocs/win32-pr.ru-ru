---
title: Сообщение EM_SETTARGETDEVICE (RichEdit. h)
description: Задает целевое устройство и толщину линии, используемые для \ 0034; что вы получаете \ 0034; (WYSIWYG) форматирование в элементе управления Rich Edit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- элементы управления Windows сообщений EM_SETTARGETDEVICE
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a3cd4e59f3800b91fedee446e927ab0ec39988474752561a04dace5572ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697594"
---
# <a name="em_settargetdevice-message"></a>\_Сообщение СЕТТАРЖЕТДЕВИЦЕ EM

Задает целевое устройство и толщину линии, используемой для "что вы видите" (WYSIWYG) в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

HDC для целевого устройства.

</dd> <dt>

*lParam* 
</dt> <dd>

Толщина линии, используемой для форматирования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение равно нулю, если операция завершается с ошибкой, или ненулевой, если она завершается успешно.

## <a name="remarks"></a>Remarks

Параметр HDC для принтера по умолчанию можно получить следующим образом.


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



Если значение *lParam* равно нулю, разрывы строк не создаются.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





