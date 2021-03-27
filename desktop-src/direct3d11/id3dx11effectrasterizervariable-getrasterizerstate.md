---
title: Метод ID3DX11EffectRasterizerVariable Жетрастеризерстате (D3dx11effect. h)
description: Получение указателя на интерфейс средства программной прорисовки.
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- Метод Жетрастеризерстате Direct3D 11
- Метод Жетрастеризерстате Direct3D 11, интерфейс ID3DX11EffectRasterizerVariable
- Интерфейс ID3DX11EffectRasterizerVariable Direct3D 11, метод Жетрастеризерстате
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972140a8f74a3e5a6728429faddacc253aaa6c9d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987260"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a>Метод ID3DX11EffectRasterizerVariable:: Жетрастеризерстате

Получение указателя на интерфейс средства программной прорисовки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индексировать в массив интерфейсов средства прорисовки. Если имеется только один интерфейс, используйте значение 0.

</dd> <dt>

*ппрастеризерстате* 
</dt> <dd>

Тип: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***

Адрес указателя на интерфейс средства растеризации (см. [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Примечания

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

