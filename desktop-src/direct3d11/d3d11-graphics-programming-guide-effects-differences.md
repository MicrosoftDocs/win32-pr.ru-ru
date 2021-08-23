---
title: Различия между эффектами 10 и Effects 11
description: В этом разделе показаны различия между эффектами 10 и 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b488015deae8cc93b9bc692c49d66ff1510bcc5639047fe253265be5b382a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990124"
---
# <a name="differences-between-effects-10-and-effects-11"></a>Различия между эффектами 10 и Effects 11

В этом разделе показаны различия между эффектами 10 и 11.

## <a name="device-contexts-threading-and-cloning"></a>Контексты устройств, потоки и клонирование

Интерфейс ID3D10Device разделен на два интерфейса в Direct3D 11: ID3D11Device и ссылку ID3D11DeviceContext. Можно создать несколько ID3D11DeviceContexts, чтобы упростить параллельное выполнение в нескольких потоках. Эффекты 11 расширяют эту концепцию до платформы Effects.

Среда выполнения Effects 11 является однопотоковой. По этой причине не следует использовать один экземпляр ID3DX11Effect с несколькими потоками одновременно.

Чтобы использовать среду выполнения Effects 11 на нескольких экземплярах, необходимо создать отдельные экземпляры ID3DX11Effect. Так как ссылку ID3D11DeviceContext также является однопотоковым, необходимо передавать разные экземпляры ссылку ID3D11DeviceContext в каждый экземпляр Effect в Apply. Эти отдельные контексты устройств можно использовать для создания списков команд, чтобы поток отрисовки мог применить их к контексту немедленного устройства.

Самый простой способ создать несколько эффектов, которые инкапсулируют одну и ту же функциональность для использования в нескольких потоках, — создать один эффект, а затем создать клонированные копии. Клонирование имеет следующие преимущества по сравнению с созданием нескольких копий с нуля:

1.  Подпрограммы клонирования выполняются быстрее, чем подпрограммы создания.
2.  Клонированные эффекты совместно используют созданные шейдеры, блоки состояний и экземпляры классов (поэтому их не нужно создавать повторно).
3.  Клонированные эффекты могут совместно использовать буферы констант.
4.  Клонированные эффекты начинаются с состояния, которое соответствует текущему эффекту (значения переменных, независимо от того, была ли она оптимизирована).

Дополнительные сведения см. [в разделе клонирование влияния](d3d11-graphics-programming-guide-effects-cloning.md) .

## <a name="effect-pools-and-groups"></a>Пулы и группы эффектов

До сих пор наиболее распространенным использованием пулов эффектов в Direct3D 10 было для группирования материалов. Пулы эффектов были удалены из эффектов 11, а группы были добавлены, что является более эффективным способом группирования материалов.

Группа эффектов — это просто набор приемов. Дополнительные сведения см. в разделе [синтаксис группы эффектов (Direct3D 11)](d3d11-effect-group-syntax.md) .

Рассмотрим следующую иерархию эффектов с четырьмя дочерними эффектами и одним пулом эффектов:


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



Вы можете добиться тех же функций в эффекте 11 с помощью групп:


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a>Новые этапы шейдера

В Direct3D 11 есть три новых этапа шейдера: шейдер поверхности, Шейдер доменов и шейдер вычислений. Эффекты 11 обрабатывают их подобным образом для шейдеров вершин, шейдеров geometry и шейдеров пикселей.

В эффекты 11 были добавлены три новых типа переменных.

-   хуллшадер
-   домаиншадер
-   компутешадер

При использовании этих шейдеров в приеме необходимо пометить этот метод «technique11», а не «technique10». Невозможно задать шейдер вычислений в том же процессе, что и любое другое графическое состояние (другие шейдеры, блоки состояний или целевые объекты прорисовки).

## <a name="new-texture-types"></a>Новые типы текстур

Direct3D 11 поддерживает следующие типы текстур:

-   [аппендструктуредбуффер](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [битеаддрессбуффер](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [консуместруктуредбуффер](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [структуредбуффер](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>Представления неупорядоченного доступа

Эффекты 11 поддерживают получение и установку новых типов представлений неупорядоченного доступа. Это работает аналогично текстурам.

Рассмотрим этот эффект в HLSL примере:


```
  
RWTexture1D<float> myUAV;
```



Эту переменную можно задать в C++ следующим образом:


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



Direct3D 11 поддерживает следующие неупорядоченные типы представлений доступа:

-   рвбуффер
-   рвбитеаддрессбуффер
-   рвструктуредбуффер
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>Интерфейсы и экземпляры классов

Синтаксис интерфейса и класса см. в разделе [интерфейсы и классы](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Сведения об использовании интерфейсов и классов в эффектах см. [в разделе интерфейсы и классы в эффектах](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).

## <a name="addressable-stream-out"></a>Исходящий поток с адресацией

В Direct3D 10 шейдеры Geometry могут выводить один поток данных в блок вывода потока и в блок средства прорисовки. В Direct3D11 шейдеры Geometry могут выводить до четырех потоков данных в выходную единицу потока и не более одного из этих потоков в блок средства прорисовки. Встроенная функция **конструктгсвиссо** была обновлена для отражения этой новой функциональности.

Дополнительные сведения см. в разделе [потоковая передача синтаксиса](d3d11-graphics-reference-effect-streamout.md) .

## <a name="setting-and-unsetting-device-state"></a>Установка и сброс состояния устройства

В эффектах 10 можно сделать буферы констант и буферы текстур управляемыми пользователем с помощью функций [**ID3D10EffectConstantBuffer:: сетконстантбуффер**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) и [**сеттекстуребуффер**](id3dx11effectconstantbuffer-settexturebuffer.md) . После вызова этих функций среда выполнения Effects 10 больше не управляет буфером констант или буфером текстуры, и пользователь должен заполнить данные с помощью интерфейса ID3D10Device.

В последствиях 11 можно также сделать блоки состояния (состояние смешения, состояние средства прорисовки, состояние трафарета и состояние образца) управляемыми пользователем с помощью следующих вызовов:

-   [**ID3DX11EffectBlendVariable:: Сетблендстате**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable:: Сетрастеризерстате**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable:: СетдепсстенЦилстате**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable:: Сетсамплер**](id3dx11effectsamplervariable-setsampler.md)

После вызова этих функций среда выполнения Effects 11 больше не управляет переменными блока State, и значения останутся без изменений. Обратите внимание, что, поскольку блоки состояния являются неизменяемыми, пользователь должен задать новый блок состояния, чтобы изменить значения.

Кроме того, можно восстановить постоянные буферы, буферы текстуры и блоки состояния в неуправляемое состояние. Если вы отмените установку этих переменных, среда выполнения Effects 11 продолжит обновлять их при необходимости. Для неограниченного использования пользовательских переменных можно использовать следующие вызовы:

-   [**ID3DX11EffectConstantBuffer:: Ундосетконстантбуффер**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer:: Ундосеттекстуребуффер**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable:: Ундосетблендстате**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable:: Ундосетрастеризерстате**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable:: УндосетдепсстенЦилстате**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable:: Ундосетсамплер**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>Воздействие виртуальной машины

Виртуальная машина Effects, которая вычисляет сложные выражения вне функций, была удалена.

Следующие примеры сложных выражений не поддерживаются:

1.  Сетпикселшадер (Мипсаррай (i \* 3 + j));
2.  Сетпикселшадер (Мипсаррай ((float) i);
3.  ФИЛЬТР = i + 2;

Поддерживаются следующие примеры несложных выражений:

1.  Сетпикселшадер (МИПС);
2.  Сетпикселшадер (МИПС \[ i \] );
3.  Сетпикселшадер (МИПС \[ уиндекс \] );//уиндекс является переменной uint
4.  ФИЛЬТР = i;
5.  FILTER = АНИЗОТРОПНЫЙ;

Эти выражения могут появляться в выражениях блока состояния (например, FILTER) и в выражениях передачи (например, Сетпикселшадер).

## <a name="source-availability-and-location"></a>Доступность источника и расположение

Эффекты 10 были распространены в D3D10.dll. эффекты 11 распространяются в виде источника, с соответствующими Visual Studio решениями для его компиляции. При создании приложений типа Effects рекомендуется включать источник Effects 11 непосредственно в эти приложения.

Вы можете получить эффекты 11 от [эффектов обновления Direct3D 11](https://github.com/Microsoft/FX11).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Эффекты (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 