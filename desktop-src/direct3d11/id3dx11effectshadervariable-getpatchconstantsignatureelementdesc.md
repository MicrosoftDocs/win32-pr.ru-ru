---
title: Метод ID3DX11EffectShaderVariable Жетпатчконстантсигнатурилементдеск (D3dx11effect. h)
description: Получить описание подписи константы исправлений.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- Метод Жетпатчконстантсигнатурилементдеск Direct3D 11
- Метод Жетпатчконстантсигнатурилементдеск Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетпатчконстантсигнатурилементдеск
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85adc4a022c0f897a2e228aab670ccae60de0ec256e5f88e033991b137863fe1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565874"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a>Метод ID3DX11EffectShaderVariable:: Жетпатчконстантсигнатурилементдеск

Получить описание подписи константы исправлений.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPatchConstantSignatureElementDesc(
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

 

