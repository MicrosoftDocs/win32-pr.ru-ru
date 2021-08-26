---
title: Структура D3DX11_EFFECT_SHADER_DESC (D3dx11effect. h)
description: Описывает шейдер эффектов.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48695b2e6ff0cca2046606eaad7dbdf137641ce126bd4f5f211e399aaf29d39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096354"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>\_ \_ Структура построителя шейдеров D3DX11 Effect \_

Описывает шейдер эффектов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**пинпутсигнатуре**
</dt> <dd>

Тип: **Константный [**байт**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Передано в Креатеинпутлайаут. Допустим только для шейдера вершин или шейдера Geometry. См. раздел [**ID3D11Device:: креатеинпутлайаут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).

</dd> <dt>

**исинлине**
</dt> <dd>

Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**Значение true** , если шейдер определяется встроенным; в противном случае — **false**.

</dd> <dt>

**пбитекоде**
</dt> <dd>

Тип: **Константный [**байт**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Байтовый код шейдера.

</dd> <dt>

**битекоделенгс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Длина Пбитекоде.

</dd> <dt>

**содеклс**
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Потоковая строка объявления (для шейдера Geometry с таким образом).

</dd> <dt>

**растеризедстреам**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Указывает, какой поток является растровым. Шейдеры D3D11 Geometry могут выводить до четырех потоков данных, один из которых может быть растрирования.

</dd> <dt>

**нуминпутсигнатуринтриес**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число записей во входной подписи.

</dd> <dt>

**нумаутпутсигнатуринтриес**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число записей в выходной подписи.

</dd> <dt>

**нумпатчконстантсигнатуринтриес**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число записей в сигнатуре константы исправления.

</dd> </dl>

## <a name="remarks"></a>Remarks

D3DX11 \_ Effect \_ Shader \_ DESC используется с [**ID3DX11EffectShaderVariable:: жетшадердеск**](id3dx11effectshadervariable-getshaderdesc.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

