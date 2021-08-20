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
ms.openlocfilehash: b9ebe2849346eb85b934c93b1d79b6ab0c43744ff60f5cf056d05edf63d1ce0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989854"
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

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





