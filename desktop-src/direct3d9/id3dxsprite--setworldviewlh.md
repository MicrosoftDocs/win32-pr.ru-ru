---
description: Задает для спрайта левое преобразование представления мира. Перед объявлением или сортировкой спрайтов необходимо вызвать этот метод.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: 'Метод ID3DXSprite:: Сетворлдвиевлх (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397c3803f6d4e445f74a8b24a61e86e72e471648
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273840"
---
# <a name="id3dxspritesetworldviewlh-method"></a>Метод ID3DXSprite:: Сетворлдвиевлх

Задает для спрайта левое преобразование представления мира. Перед объявлением или сортировкой спрайтов необходимо вызвать этот метод.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пворлд* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на [**D3DXMATRIX**](d3dxmatrix.md) , содержащий универсальное преобразование. Если **значение равно NULL**, то для универсального преобразования используется матрица идентификаторов.

</dd> <dt>

*pView* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на [**D3DXMATRIX**](d3dxmatrix.md) , содержащий преобразование представления. Если **значение равно NULL**, то для преобразования представления используется матрица идентификаторов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="remarks"></a>Комментарии

Вызов этого метода (или to [**ID3DXSprite:: сетворлдвиеврх**](id3dxsprite--setworldviewrh.md)) требуется, если спрайт будет подготовлен к просмотру с помощью [ \_ \_ объявления D3DXSprite](d3dxsprite.md), D3DXSprite \_ \_ сортировки \_ глубины \_ Фронттобакк или D3DXSprite \_ \_ сортировки \_ глубины \_ бакктофронт в [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




