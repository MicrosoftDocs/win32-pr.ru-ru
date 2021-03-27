---
description: Вызывается, когда окно регистрируется как окно оболочки.
title: Дшеллвиндовсевентс. Виндоврегистеред, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987590"
---
# <a name="dshellwindowseventswindowregistered-method"></a>Дшеллвиндовсевентс. Виндоврегистеред, метод

Вызывается, когда окно регистрируется как окно оболочки.

## <a name="syntax"></a>Синтаксис


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лкукие* \[ окне\]
</dt> <dd>

Тип: **Integer**

Файл cookie, определяющий зарегистрированное окно.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Примечания

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

[**виндовревокед**](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[**Регистрация**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[**регистерпендинг**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




