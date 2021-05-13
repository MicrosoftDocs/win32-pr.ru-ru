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
ms.openlocfilehash: 7ed78dcaa545b2321b04aff9ff2f4e711f93c992
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843185"
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

## <a name="requirements"></a>Requirements (Требования)



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

[**Revoke**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




