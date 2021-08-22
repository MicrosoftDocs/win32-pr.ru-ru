---
title: Метод ID3DX11EffectTechnique-desc (D3dx11effect. h)
description: Получите описание метода.
ms.assetid: ed82d873-0540-4aa8-ac0f-198852b886ad
keywords:
- Метод DESC Direct3D 11
- Метод DESC Direct3D 11, интерфейс ID3DX11EffectTechnique
- ID3DX11EffectTechnique интерфейс Direct3D 11, метод DESC
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad72387b59690d747d5b86927062e8ee8a0ec51ba2f81d746112d65e72d5782f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532532"
---
# <a name="id3dx11effecttechniquegetdesc-method"></a>Метод ID3DX11EffectTechnique:: DESC

Получите описание метода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDesc(
   D3DX11_TECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдеск* 
</dt> <dd>

Тип: **[ **D3DX11 \_ техника \_ DESC**](d3dx11-technique-desc.md)\***

Указатель на описание метода (см. [**метод D3DX11 \_ \_ DESC**](d3dx11-technique-desc.md)).

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

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





