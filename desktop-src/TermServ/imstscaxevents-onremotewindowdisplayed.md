---
title: Имстскаксевентс Онремотевиндовдисплайед, метод
description: Вызывается при отображении окна RemoteApp.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онремотевиндовдисплайед
- Службы удаленных рабочих столов метода Онремотевиндовдисплайед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онремотевиндовдисплайед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415756"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>Метод Имстскаксевентс:: Онремотевиндовдисплайед

Вызывается при отображении окна RemoteApp.

## <a name="syntax"></a>Синтаксис


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*вбдисплайед* \[ окне\]
</dt> <dd>

Тип: **Variant \_ bool**

Указывает, отображается ли окно RemoteApp или скрыто.

</dd> <dt>

*HWND* \[ окне\]
</dt> <dd>

Тип: **HWND**

Отображаемый маркер окна.

</dd> <dt>

*виндоваттрибуте* \[ окне\]
</dt> <dd>

Тип: **[ **ремотевиндовдисплайедаттрибуте**](remotewindowdisplayedattribute.md)**

Значение перечисления [**ремотевиндовдисплайедаттрибуте**](remotewindowdisplayedattribute.md) , которое указывает дополнительные сведения о событии.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ремотевиндовдисплайедаттрибуте**](remotewindowdisplayedattribute.md)
</dt> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





