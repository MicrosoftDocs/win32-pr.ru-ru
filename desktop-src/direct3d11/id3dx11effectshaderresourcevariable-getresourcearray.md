---
title: Метод ID3DX11EffectShaderResourceVariable Жетресаурцеаррай (D3dx11effect. h)
description: Получение массива ресурсов шейдера.
ms.assetid: 7540183d-dabb-46c2-8df1-6d4734b77f25
keywords:
- Метод Жетресаурцеаррай Direct3D 11
- Метод Жетресаурцеаррай Direct3D 11, интерфейс ID3DX11EffectShaderResourceVariable
- Интерфейс ID3DX11EffectShaderResourceVariable Direct3D 11, метод Жетресаурцеаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResourceArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0caa1ed7fabd6f5d570ceb646164c86b91d4687456ed1711f1cf5d81a42c733c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460844"
---
# <a name="id3dx11effectshaderresourcevariablegetresourcearray-method"></a>Метод ID3DX11EffectShaderResourceVariable:: Жетресаурцеаррай

Получение массива ресурсов шейдера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetResourceArray(
   ID3D11ShaderResourceView **ppResources,
   UINT                     Offset,
   UINT                     Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппресаурцес* 
</dt> <dd>

Тип: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Адрес массива интерфейсов шейдера-представления ресурсов. См. [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> <dt>

*Offset* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс массива, начинающийся с нуля, для получения первого интерфейса.

</dd> <dt>

*Количество* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Количество элементов в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

