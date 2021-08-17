---
description: Вызывается при отмене регистрации окна оболочки.
title: Дшеллвиндовсевентс. Виндовревокед, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 571808962d65d25d4fb08f8d4cb57ffd1d51da67a7ba60def191edcf2fe19575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459851"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>Дшеллвиндовсевентс. Виндовревокед, метод

Вызывается при отмене регистрации окна оболочки.

## <a name="syntax"></a>Синтаксис


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лкукие* \[ окне\]
</dt> <dd>

Тип: **Integer**

Файл cookie, определяющий отозванное окно.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

При регистрации в окне оболочки ему предоставляется файл cookie. Дополнительные сведения см. в разделе [**Регистрация**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Продукт<br/> | Internet Explorer 5<br/>                                                                                           |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (версия 5.00.2014.0216 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дшеллвиндовсевентс**](dshellwindowsevents.md)
</dt> <dt>

[**виндоврегистеред**](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[**REVOKE**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




