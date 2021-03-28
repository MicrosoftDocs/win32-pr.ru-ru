---
title: Структура D3DX11_PASS_SHADER_DESC (D3dx11effect. h)
description: Описывает пройденный результат.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987200"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>\_ \_ Структура построителя шейдеров D3DX11 Pass \_

Описывает пройденный результат.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a>Участники

<dl> <dt>

**пшадервариабле**
</dt> <dd>

Тип: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

</dd> <dd>

Переменная, из которой получен этот шейдер.

</dd> <dt>

**шадериндекс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Элемент Пшадервариабле (если массив) или 0, если не применимо.

</dd> </dl>

## <a name="remarks"></a>Примечания

D3DX11 \_ Pass \_ Shader \_ DESC используется с методами [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* шадердеск.

Если это назначение встроенного шейдера, возвращаемым интерфейсом будет анонимная переменная шейдера, которая не может быть извлечена другим способом. Его имя в описании переменной будет «$Anonymous». Если в блоке Pass нет назначения этого типа, Пшадервариабле! = **null**, но пшадервариабле->IsValid () = = **false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

