---
description: Добавляет набор эффектов анимации к контроллеру анимации.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: 'Метод ID3DXAnimationController:: Регистераниматионсет (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c6572b4a09967f2a911ffb3b147f3786aae75d71650d4d77d0564c1dbefc5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296984"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a>Метод ID3DXAnimationController:: Регистераниматионсет

Добавляет набор эффектов анимации к контроллеру анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*панимсет* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Указатель на добавляемый набор анимации [**ID3DXAnimationSet**](id3dxanimationset.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




