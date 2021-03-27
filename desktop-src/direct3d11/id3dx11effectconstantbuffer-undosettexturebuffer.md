---
title: Метод ID3DX11EffectConstantBuffer Ундосеттекстуребуффер (D3dx11effect. h)
description: Восстанавливает ранее установленный буфер текстуры.
ms.assetid: 982e7899-9569-4611-9fe0-b78624acba2c
keywords:
- Метод Ундосеттекстуребуффер Direct3D 11
- Метод Ундосеттекстуребуффер Direct3D 11, интерфейс ID3DX11EffectConstantBuffer
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, метод Ундосеттекстуребуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5e1e1b2be167466da5a4d92999646bb7c8f225
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355260"
---
# <a name="id3dx11effectconstantbufferundosettexturebuffer-method"></a>Метод ID3DX11EffectConstantBuffer:: Ундосеттекстуребуффер

Восстанавливает ранее установленный буфер текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UndoSetTextureBuffer();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

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

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





