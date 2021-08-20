---
title: Метод ID3DX11EffectConstantBuffer Жетконстантбуффер (D3dx11effect. h)
description: Получение постоянного буфера.
ms.assetid: 857b3dc2-41ae-4a52-904a-9ca8f0afeb9e
keywords:
- Метод Жетконстантбуффер Direct3D 11
- Метод Жетконстантбуффер Direct3D 11, интерфейс ID3DX11EffectConstantBuffer
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, метод Жетконстантбуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e573b867f3ee37b6fe1633dc03982d6cf14499a30340210d21339a6e44aa305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046422"
---
# <a name="id3dx11effectconstantbuffergetconstantbuffer-method"></a>Метод ID3DX11EffectConstantBuffer:: Жетконстантбуффер

Получение постоянного буфера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetConstantBuffer(
   ID3D11Buffer **ppConstantBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппконстантбуффер* 
</dt> <dd>

Тип: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***

Адрес указателя на интерфейс постоянного буфера. См. [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).

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

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





