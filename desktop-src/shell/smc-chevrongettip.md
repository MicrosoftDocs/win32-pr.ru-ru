---
description: Запрашивает заголовок и текст всплывающей подсказки для элемента, указанного сопутствующей структурой СМДАТА.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Сообщение SMC_CHEVRONGETTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e64636994743d4b13a96fe75947fb515c4dbd3edcc94e6dee0fa85efb8bc9d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968243"
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

## <a name="remarks"></a>Remarks

Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




