---
title: IMsRdpClientNonScriptable5 Жетремотемониторсбаундингбокс, свойство
description: Задает ограничивающий прямоугольник удаленного монитора.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Жетремотемониторсбаундингбокс
- Службы удаленных рабочих столов свойства Жетремотемониторсбаундингбокс, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Жетремотемониторсбаундингбокс
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b308bf95389dcf043e87565be365ec69ecc34500ac187ee11a679349f18ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129892"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a>Свойство IMsRdpClientNonScriptable5:: Жетремотемониторсбаундингбокс

Задает ограничивающий прямоугольник удаленного монитора.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a>Значение свойства

Получает левую границу прямоугольника.

Получает верхний край прямоугольника.

Получает правую границу прямоугольника.

Получает нижнюю границу прямоугольника.

## <a name="remarks"></a>Remarks

Все координаты находятся в координатах виртуального экрана, которые находятся относительно левого верхнего угла основного монитора. Если это не основной монитор, некоторые или все из этих значений могут быть отрицательными.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                             |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





