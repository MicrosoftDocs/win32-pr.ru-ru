---
description: Создает объект Sprite, связанный с определенным устройством. Объекты Sprite используются для рисования 2D-изображений на экране.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: Функция D3DXCreateSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713695"
---
# <a name="d3dxcreatesprite-function"></a>Функция D3DXCreateSprite

Создает объект Sprite, связанный с определенным устройством. Объекты Sprite используются для рисования 2D-изображений на экране.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , устройство, связываемое с спрайтом.

</dd> <dt>

*ппсприте* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***

Адрес указателя на интерфейс [**ID3DXSprite**](id3dxsprite.md) . Этот интерфейс позволяет пользователю получить доступ к функциям спрайта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Этот интерфейс можно использовать для рисования двух трехмерных изображений в пространстве экрана связанного устройства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
