---
title: Метод ID3DX11EffectShaderVariable Жетаутпутсигнатурилементдеск (D3dx11effect. h)
description: Получение описания выходной подписи.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- Метод Жетаутпутсигнатурилементдеск Direct3D 11
- Метод Жетаутпутсигнатурилементдеск Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетаутпутсигнатурилементдеск
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetOutputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af968b25a00e32b489a520e9d4a3e870329af910caa8ac1bf45ac49a7ea6132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533270"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a>Метод ID3DX11EffectShaderVariable:: Жетаутпутсигнатурилементдеск

Получение описания выходной подписи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetOutputSignatureElementDesc(
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

Индекс элемента, начинающийся с нуля.

</dd> <dt>

*пдеск* 
</dt> <dd>

Тип: **[ **\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Указатель на описание параметра (см. раздел [**\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Результат содержит один или несколько шейдеров; Каждый шейдер имеет входную и выходную сигнатуру; Каждая сигнатура содержит один или несколько элементов (или параметров). Индекс шейдера определяет шейдер, а индекс элемента определяет элемент (или параметр) в сигнатуре шейдера.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

