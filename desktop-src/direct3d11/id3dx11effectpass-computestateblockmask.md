---
title: Метод ID3DX11EffectPass Компутестатеблоккмаск (D3dx11effect. h)
description: Создание маски для разрешения или запрета изменений состояния.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Метод Компутестатеблоккмаск Direct3D 11
- Метод Компутестатеблоккмаск Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Компутестатеблоккмаск
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987038"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a>Метод ID3DX11EffectPass:: Компутестатеблоккмаск

Создание маски для разрешения или запрета изменений состояния.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстатеблоккмаск* 
</dt> <dd>

Тип: **[ **D3DX11 \_ \_ \_ Маска блока состояния**](d3dx11-state-block-mask.md)\***

Указатель на маску блока State (см. раздел [**\_ \_ \_ Маска блока состояния D3DX11**](d3dx11-state-block-mask.md)).

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





