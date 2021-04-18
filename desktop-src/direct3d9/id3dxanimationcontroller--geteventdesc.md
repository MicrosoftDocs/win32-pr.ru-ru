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
ms.openlocfilehash: 9f717c032358dd921be2df1c8a84d1aa02a7a93a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713955"
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
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




