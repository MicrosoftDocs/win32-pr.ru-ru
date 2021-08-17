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
ms.openlocfilehash: 7ad7270f9054b875eabcb1fd9f5a7ab2e299a5916d55ef4630988921b6b2f4ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455574"
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

[**виндовревокед**](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[**Зарегистрировать**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[**регистерпендинг**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




