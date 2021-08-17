---
title: Синтаксис объявления функций
description: Функции HLSL объявляются с помощью следующего синтаксиса.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce8c6ec83963dac74dce32d248b23548c767192a604ddb8afbe35cf932dedee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514609"
---
# <a name="function-declaration-syntax"></a>Синтаксис объявления функций

Функции HLSL объявляются с помощью следующего синтаксиса.

\[*Сторажекласс* \] \[клиппланес () \] \[ точное \] \_ *имя* возвращаемого значения ( \[ *ArgumentList* \] ) \[ : *семантика* \] { \[ *статементблокк* \] };



 

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*сторажекласс*
</dt> <dd>

Модификатор, который переопределяет объявление функции. в настоящее время **подставляемое** значение является единственным значением модификатора. Значение модификатора должно быть **встроенным** , поскольку оно также является значением по умолчанию. Поэтому функция является встроенной, независимо от того, задано ли значение **inline**, и все функции в HLSL являются встроенными. Встроенная функция создает копию тела функции (при компиляции) для каждого вызова функции. Это делается для снижения издержек при вызове функции.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*клиппланес*
</dt> <dd>

Необязательный список плоскостей, который имеет до 6 заданных пользователем плоскостей. Это альтернативный механизм для [SV \_ клипдистанце](dx-graphics-hlsl-semantics.md) , который работает на [уровне функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x и выше.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*
</dt> <dd>

Строка ASCII, однозначно определяющая имя функции шейдера.

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*
</dt> <dd>

Необязательный список аргументов, который представляет собой разделенный запятыми список [аргументов](dx-graphics-hlsl-function-parameters.md) , передаваемых в функцию.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Семантическ*
</dt> <dd>

Необязательная строка, которая определяет предполагаемое использование возвращаемых данных (см. раздел [семантика (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*статементблокк*
</dt> <dd>

Необязательные [инструкции](dx-graphics-hlsl-statement-blocks.md) , составляющие тело функции. Функция, определенная без тела, называется прототипом функции; тело функции прототипа должно быть определено в любом расположении, прежде чем можно будет вызвать функцию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип возвращаемого значения может быть любым из следующих [типов HLSL](dx-graphics-hlsl-data-types.md).

## <a name="remarks"></a>Remarks

Синтаксис на этой странице описывает почти все типы функций HLSL, включая шейдеры вершин, шейдеры пикселей и вспомогательные функции. Хотя шейдер Geometry также реализован с помощью функции, его синтаксис немного сложнее, поэтому существует отдельная страница, определяющая объявление функции шейдера Geometry (см. раздел [объект Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).

Функцию можно перегрузить при условии, что ей присваивается уникальное сочетание типов параметров и (или) порядка параметров. HLSL также реализует ряд встроенных или [**встроенных функций**](dx-graphics-hlsl-intrinsic-functions.md).

С помощью атрибута **клиппланес** можно указать определенные пользователем плоскости. Windows применяет эти элементы обрезки ко всем рисуемым примитивам. Атрибут **клиппланес** работает так же, как [SV \_ клипдистанце](dx-graphics-hlsl-semantics.md) , но работает на всех [уровнях компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) оборудования 9 \_ x и выше. Дополнительные сведения см. [в статье пользовательские ролики на устройствах на уровне компонентов 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="examples"></a>Примеры

Этот пример относится к BasicHLSL10. FX из [примера BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



В этом примере из Адванцедпартиклес. FX из [примера адванцедпартиклес](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)демонстрируется использование семантики для возвращаемого типа.


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
