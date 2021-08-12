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
ms.openlocfilehash: 8ec7328ce346b51c3315086dcc193f421081dd77fc3a169bc448fba10bc7fa3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536847"
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



## <a name="members"></a>Члены

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

## <a name="remarks"></a>Remarks

D3DX11 \_ Pass \_ Shader \_ DESC используется с методами [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* шадердеск.

Если это назначение встроенного шейдера, возвращаемым интерфейсом будет анонимная переменная шейдера, которая не может быть извлечена другим способом. Его имя в описании переменной будет «$Anonymous». Если в блоке Pass нет назначения этого типа, Пшадервариабле! = **null**, но пшадервариабле->IsValid () = = **false**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

