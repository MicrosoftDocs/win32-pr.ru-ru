---
description: Возвращает описание указанного события анимации.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'Метод ID3DXAnimationController:: Жетевентдеск (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc113788a8eb6b64accfcba8c58dd3a3512e17601ec02ce5dd33349628c69212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987944"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a>Метод ID3DXAnimationController:: Жетевентдеск

Возвращает описание указанного события анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Хевент* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик события анимации для описания.

</dd> <dt>

*пдеск* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXEVENT \_ DESC**](d3dxevent-desc.md)**

Указатель на структуру [**D3DXEVENT \_ DESC**](d3dxevent-desc.md) , содержащую описание события анимации.

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

 

 




