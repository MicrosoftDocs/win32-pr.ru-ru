---
title: Интерфейсы и классы в эффектах
description: Существует множество способов использования классов и интерфейсов в влиянии 11.
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413166"
---
# <a name="interfaces-and-classes-in-effects"></a>Интерфейсы и классы в эффектах

Существует множество способов использования классов и интерфейсов в влиянии 11. Синтаксис интерфейса и класса см. в разделе [интерфейсы и классы](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

В следующих разделах подробно описано, как указать экземпляры класса для шейдера, использующего интерфейсы. В примерах мы будем использовать следующий интерфейс и классы:


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



Обратите внимание, что экземпляры интерфейса можно инициализировать экземплярами класса. Массивы экземпляров классов и интерфейсов также поддерживаются, и их можно инициализировать, как показано в следующем примере:


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a>Параметры универсального интерфейса

Как и другие однородные типы данных, параметры универсального интерфейса должны быть указаны в вызове Компилешадер. Параметры интерфейса могут быть назначены глобальным экземплярам интерфейса или экземплярам глобальных классов. При назначении глобальному экземпляру интерфейса шейдер будет иметь зависимость от экземпляра интерфейса, что означает, что для него должен быть задан экземпляр класса. При назначении экземплярам глобального класса компилятор специализирует шейдер (как с другими универсальными типами данных) для использования этого класса. Это важно для двух сценариев:

1.  Шейдеры с \_ целевым объектом 4 x могут использовать параметры интерфейса, если эти параметры являются универсальными и назначены глобальным экземплярам класса (поэтому динамическая компоновка не используется).
2.  Пользователи могут принимать решение о наличии многих скомпилированных, специализированных шейдеров без динамической компоновки или нескольких скомпилированных шейдеров с динамической компоновкой.


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



Если pIColor2 остается неизменным через API, то предыдущие два прохода функционально эквивалентны, но первый использует \_ статический шейдер PS 4 0, \_ а второй использует \_ шейдер PS 5 \_ 0 с динамической компоновкой. Если pIColor2 изменяется с помощью API Effects (см. раздел Установка экземпляров класса ниже), то поведение шейдера пикселей во втором проходе может измениться.

## <a name="non-uniform-interface-parameters"></a>Параметры неоднородного интерфейса

Параметры неоднородного интерфейса создают зависимости интерфейсов для шейдеров. При применении шейдера с параметрами интерфейса эти параметры должны быть назначены в вызове Биндинтерфацес. Экземпляры глобальных интерфейсов и экземпляры глобальных классов можно указать в вызове Биндинтерфацес.


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



Если pIColor2 остается неизменным через API, предыдущие два прохода функционально эквивалентны и используют динамическую компоновку. Если pIColor2 изменяется с помощью API Effects (см. раздел Установка экземпляров класса ниже), то поведение шейдера пикселей во втором проходе может измениться.

## <a name="setting-class-instances"></a>Установка экземпляров класса

При настройке шейдера с помощью динамической компоновки шейдера для устройства Direct3D 11 необходимо также указать экземпляры класса. При задании такого шейдера с **пустым** экземпляром класса возникает ошибка. Таким образом, все экземпляры интерфейса, на которые ссылается шейдер, должны иметь связанный экземпляр класса.

В следующем примере показано, как получить переменную экземпляра класса из действия и задать ее для переменной интерфейса:


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Эффекты (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 