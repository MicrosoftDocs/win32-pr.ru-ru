---
title: Структура D3DX11_PASS_DESC (D3dx11effect. h)
description: Описывает пройденный результат, который содержит состояние конвейера.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987203"
---
# <a name="d3dx11_pass_desc-structure"></a>\_Структура D3DX11 Pass \_ DESC

Описывает пройденный результат, который содержит состояние конвейера.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a>Участники

<dl> <dt>

**имя**;
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Имя этого этапа (**null** , если он не является анонимным).

</dd> <dt>

**Заметки**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число заметок на этом проходе.

</dd> <dt>

**пиаинпутсигнатуре**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

Сигнатура из шейдера вершин или шейдера Geometry (Если шейдер вершин отсутствует) или **значение NULL** , если ни один из них не существует.

</dd> <dt>

**иаинпутсигнатуресизе**
</dt> <dd>

Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Размер сингатуре в байтах.

</dd> <dt>

**стенЦилреф**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Значение ссылки на набор элементов, используемое в состоянии трафарета глубины.

</dd> <dt>

**самплемаск**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Образец маски для состояния смешения.

</dd> <dt>

**блендфактор**
</dt> <dd>

Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Коэффициенты смешения для каждого компонента (RGBA) для состояния смешения.

</dd> </dl>

## <a name="remarks"></a>Примечания

D3DX11 \_ Pass \_ DESC используется с [**ID3DX11EffectPass:: DESC**](id3dx11effectpass-getdesc.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

