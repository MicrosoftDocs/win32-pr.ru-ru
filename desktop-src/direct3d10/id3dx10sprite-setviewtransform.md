---
description: Задайте преобразование представления, которое применяется ко всем спрайтам.
ms.assetid: 0420b141-46c7-4409-a0c4-67d1e8e02cd4
title: 'Метод ID3DX10Sprite:: Сетвиевтрансформ (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62ec2129d441acaa0719d2e64c02b4cc57370c8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704031"
---
# <a name="id3dx10spritesetviewtransform-method"></a>Метод ID3DX10Sprite:: Сетвиевтрансформ

Задайте преобразование представления, которое применяется ко всем спрайтам.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetViewTransform(
  [in] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвиевтрансформ* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на D3DXMATRIX, содержащий преобразование спрайта из исходного мира. Используйте это преобразование для масштабирования, вращения или преобразования спрайта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
