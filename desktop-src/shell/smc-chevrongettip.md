---
description: Запрашивает заголовок и текст всплывающей подсказки для элемента, указанного сопутствующей структурой СМДАТА.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Сообщение SMC_CHEVRONGETTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985748"
---
# <a name="smc_chevrongettip-message"></a>\_Сообщение SMC чевронжеттип

Запрашивает заголовок и текст всплывающей подсказки для элемента, указанного сопутствующей структурой [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзтиптитле* 
</dt> <dd>

Указатель на буфер, который получает строку в Юникоде, завершающуюся **нулем**, которая содержит заголовок подсказки. Длина этой строки не должна превышать максимальное число \_ символов в пути, включая завершающий символ **null** .

</dd> <dt>

*пвсзтиптекст* 
</dt> <dd>

Указатель на буфер, который получает строку в Юникоде, завершающуюся **нулем**, которая содержит текст подсказки. Длина этой строки не должна превышать максимальное число \_ символов в пути, включая завершающий символ **null** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвратите \_ ОК.

## <a name="remarks"></a>Примечания

Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




