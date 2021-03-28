---
title: msad4
description: Сравнивает 4-байтное ссылочное значение и 8-байтовое исходное значение и накапливает вектор с 4 суммами. Каждая сумма соответствует маскированной сумме абсолютных различий между значением ссылки и исходным значением.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- msad4 HLSL
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104984144"
---
# <a name="msad4"></a>msad4

Сравнивает 4-байтное ссылочное значение и 8-байтовое исходное значение и накапливает вектор с 4 суммами. Каждая сумма соответствует маскированной сумме абсолютных различий между значением ссылки и исходным значением.



| uint4 Result = msad4 (ссылка uint, источник uint2, накопленный uint4); |
|------------------------------------------------------------------|



 

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="reference"></span><span id="REFERENCE"></span>*IsReference*
</dt> <dd>

\[в \] массиве ссылок 4 байта в одном значении **uint** .

</dd> <dt>

<span id="source"></span><span id="SOURCE"></span>*источника*
</dt> <dd>

\[в \] исходном массиве из 8 байт в двух значениях **uint2** .

</dd> <dt>

<span id="accum"></span><span id="ACCUM"></span>*накоплен*
</dt> <dd>

\[в \] векторе из 4 значений. **msad4** добавляет этот вектор к маскированной сумме абсолютных различий между значением ссылки и исходным значением.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Вектор из 4 сумм. Каждая сумма соответствует маскированной сумме абсолютных различий между значением ссылки и исходным значением. **msad4** не содержит разницы в сумме, если это различие замаскировано (то есть ссылочный байт равен 0).

## <a name="remarks"></a>Примечания

Чтобы использовать встроенную функцию **msad4** в коде шейдера, вызовите метод [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) с [**\_ \_ \_ параметром D3D11 Feature D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) , чтобы убедиться, что устройство Direct3D поддерживает параметр [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) . Для встроенной функции **msad4** требуется драйвер дисплея WDDM 1,2, а все драйверы дисплея WDDM 1,2 должны поддерживать **msad4**. Если приложение создает устройство отрисовки с [уровнем функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 или 11,1, а целью компиляции является модель шейдера 5 или более поздней версии, исходный код HLSL может использовать встроенную функцию **msad4** .

Возвращаемые значения точно до 65535. При вызове встроенной функции **msad4** с входными данными, которые могут привести к возвращенным значениям, превышающим 65535, **msad4** выдает неопределенные результаты.

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                | Поддерживается |
|-------------------------------------------------------------|-----------|
| [Модель шейдера 5 или более поздней версии](d3d11-graphics-reference-sm5.md) | да       |



 

## <a name="examples"></a>Примеры

Ниже приведен пример вычисления результата для **msad4**:


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



Ниже приведен пример того, как можно использовать **msad4** для поиска эталонного шаблона в буфере:


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>           |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

