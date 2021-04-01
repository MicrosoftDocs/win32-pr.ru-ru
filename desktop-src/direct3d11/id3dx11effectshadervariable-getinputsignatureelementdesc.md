---
title: Метод ID3DX11EffectShaderVariable Жетинпутсигнатурилементдеск (D3dx11effect. h)
description: Получить описание входной подписи.
ms.assetid: 45b1fd25-1005-48fd-8a61-561ea2c273e5
keywords:
- Метод Жетинпутсигнатурилементдеск Direct3D 11
- Метод Жетинпутсигнатурилементдеск Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетинпутсигнатурилементдеск
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetInputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf788370c26da1ba773d797de544b1a64750d90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157267"
---
# <a name="id3dx11effectshadervariablegetinputsignatureelementdesc-method"></a>Метод ID3DX11EffectShaderVariable:: Жетинпутсигнатурилементдеск

Получить описание входной подписи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetInputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*шадериндекс* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс шейдера, начинающийся с нуля.

</dd> <dt>

*Элемент* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс элемента шейдера, начинающийся с нуля.

</dd> <dt>

*пдеск* 
</dt> <dd>

Тип: **[ **\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Указатель на описание параметра (см. раздел [**\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Примечания

Результат содержит один или несколько шейдеров; Каждый шейдер имеет входную и выходную сигнатуру; Каждая сигнатура содержит один или несколько элементов (или параметров). Индекс шейдера определяет шейдер, а индекс элемента определяет элемент (или параметр) в сигнатуре шейдера.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

