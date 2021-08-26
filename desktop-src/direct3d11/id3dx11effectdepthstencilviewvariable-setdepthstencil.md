---
title: Метод ID3DX11EffectDepthStencilViewVariable СетдепсстенЦил (D3dx11effect. h)
description: Задайте ресурс представления глубины-набор.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Метод СетдепсстенЦил Direct3D 11
- Метод СетдепсстенЦил Direct3D 11, интерфейс ID3DX11EffectDepthStencilViewVariable
- Интерфейс ID3DX11EffectDepthStencilViewVariable Direct3D 11, метод СетдепсстенЦил
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae1e8b984bb15e083360ef99036549c534d8e047a2375ad0b0a6e5469b9191c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069684"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a>Метод ID3DX11EffectDepthStencilViewVariable:: СетдепсстенЦил

Задайте ресурс представления глубины-набор.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*исходный код* 
</dt> <dd>

Тип: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***

Указатель на интерфейс представления глубины-трафарета. См. [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





