---
title: Метод ID3DX11EffectDepthStencilVariable УндосетдепсстенЦилстате (D3dx11effect. h)
description: Восстанавливает ранее заданное состояние трафарета глубины.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Метод УндосетдепсстенЦилстате Direct3D 11
- Метод УндосетдепсстенЦилстате Direct3D 11, интерфейс ID3DX11EffectDepthStencilVariable
- Интерфейс ID3DX11EffectDepthStencilVariable Direct3D 11, метод УндосетдепсстенЦилстате
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 626c430c268c7c8c63e006bdde9e62a49d139d2212e08d7a3e4cedeea3d31722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989824"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a>Метод ID3DX11EffectDepthStencilVariable:: УндосетдепсстенЦилстате

Восстанавливает ранее заданное состояние трафарета глубины.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс в массиве интерфейсов трафарета глубины. Если имеется только один интерфейс трафарета глубины, используйте значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

