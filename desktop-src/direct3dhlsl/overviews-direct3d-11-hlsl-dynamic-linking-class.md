---
title: Интерфейсы и классы
description: В компоновке динамического шейдера используются интерфейсы и классы высокого уровня шейдеров (HLSL), которые синтаксически похожи на их аналоги C++.
ms.assetid: 124a358d-30ab-4efe-88ed-1ff277d17b25
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71410caf7d80cb9dbcd0165c753d75cc8f5cbe00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413397"
---
# <a name="interfaces-and-classes"></a>Интерфейсы и классы

В компоновке динамического шейдера используются интерфейсы и классы высокого уровня шейдеров (HLSL), которые синтаксически похожи на их аналоги C++. Это позволяет шейдеру ссылаться на абстрактные экземпляры интерфейса во время компиляции и оставлять эти экземпляры конкретным классам для приложения в среде выполнения.

В следующих разделах подробно описано, как настроить шейдер для использования интерфейсов и классов, а также как инициализировать экземпляры интерфейса в коде приложения.

-   [Объявление интерфейсов](#declaring-interfaces)
-   [Объявление классов](#declaring-classes)
-   [Объявления экземпляров интерфейса в шейдере](#interface-instance-declarations-in-a-shader)
-   [Объявления экземпляров классов в шейдере](#class-instance-declarations-in-a-shader)
-   [Инициализация экземпляров интерфейса в приложении](#initializing-interface-instances-in-an-application)
-   [См. также](#related-topics)

## <a name="declaring-interfaces"></a>Объявление интерфейсов

Интерфейс функционирует аналогичным образом для абстрактного базового класса в C++. Интерфейс объявляется в шейдере с помощью ключевого слова Interface и содержит только объявления методов. Методы, объявленные в интерфейсе, будут виртуальными методами в любых классах, производных от интерфейса. Производные классы должны реализовывать все методы, объявленные в интерфейсе. Обратите внимание, что интерфейсы являются единственным способом объявления виртуальных методов, в C++ нет виртуального ключевого слова, а классы Коннот объявляют виртуальные методы.

В следующем примере кода шейдера объявляются два интерфейса.


```
interface iBaseLight
{
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};       

interface iBaseMaterial
{
   float3 GetAmbientColor(float2 vTexcoord);
   
   float3 GetDiffuseColor(float2 vTexcoord);

   int GetSpecularPower();

};
      
```



## <a name="declaring-classes"></a>Объявление классов

Класс ведет себя аналогичным образом для классов в C++. Класс объявляется с ключевым словом class и может содержать переменные-члены и методы. Класс может наследовать от нуля или от одного класса и от нуля или нескольких интерфейсов. Классы должны реализовывать или наследовать реализации для всех интерфейсов в цепочке наследования, а также создавать экземпляры класса.

Следующий пример кода шейдера иллюстрирует создание производного класса от интерфейса и от другого класса.


```
class cAmbientLight : iBaseLight
{
   float3            m_vLightColor;     
   bool     m_bEnable;
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};

class cHemiAmbientLight : cAmbientLight
{
   float4   m_vGroundColor;
   float4   m_vDirUp;
   float3 IlluminateAmbient(float3 vNormal);
};        
      
```



## <a name="interface-instance-declarations-in-a-shader"></a>Объявления экземпляров интерфейса в шейдере

Экземпляр интерфейса выступает в качестве заполнителя для экземпляров класса, предоставляющих реализацию методов интерфейса. Использование экземпляра интерфейса позволяет коду шейдера вызывать метод, не зная, какая реализация этого метода будет вызываться. Код шейдера объявляет один или несколько экземпляров для каждого определяемого им интерфейса. Эти экземпляры используются в коде шейдера аналогичным образом для указателей базовых классов C++.

В следующем примере кода шейдера показано объявление нескольких экземпляров интерфейса и их использование в коде шейдера.


```
// Declare interface instances
iBaseLight     g_abstractAmbientLighting;
iBaseLight     g_abstractDirectLighting;
iBaseMaterial  g_abstractMaterial;

struct PS_INPUT
{
    float4 vPosition : SV_POSITION;
    float3 vNormal   : NORMAL;
    float2 vTexcoord : TEXCOORD0;
};

float4 PSMain( PS_INPUT Input ) : SV_TARGET
{ 
    float3 Ambient = (float3)0.0f;       
    Ambient = g_abstractMaterial.GetAmbientColor( Input.vTexcoord ) *         
        g_abstractAmbientLighting.IlluminateAmbient( Input.vNormal );

    float3 Diffuse = (float3)0.0f;  
    Diffuse += g_abstractMaterial.GetDiffuseColor( Input.vTexcoord ) * 
        g_abstractDirectLighting.IlluminateDiffuse( Input.vNormal );

    float3 Specular = (float3)0.0f;   
    Specular += g_abstractDirectLighting.IlluminateSpecular( Input.vNormal, 
        g_abstractMaterial.GetSpecularPower() );
     
    float3 Lighting = saturate( Ambient + Diffuse + Specular );
     
    return float4(Lighting,1.0f); 
}
```



## <a name="class-instance-declarations-in-a-shader"></a>Объявления экземпляров классов в шейдере

Каждый класс, который будет использоваться вместо экземпляра интерфейса, должен быть либо объявлен как переменная в буфере констант, либо создан приложением во время выполнения с помощью метода [**ID3D11ClassLinkage:: креатеклассинстанце**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) . Экземпляры интерфейса будут указываться в экземплярах класса в коде приложения. На экземпляры классов можно ссылаться в коде шейдера, как и любую другую переменную, но класс, производный от интерфейса, обычно используется только с экземпляром интерфейса и не будет ссылаться непосредственно на код шейдера.

В следующем примере кода шейдера показано объявление нескольких экземпляров класса.


```
cbuffer cbPerFrame : register( b0 )
{
   cAmbientLight     g_ambientLight;
   cHemiAmbientLight g_hemiAmbientLight;
   cDirectionalLight g_directionalLight;
   cEnvironmentLight g_environmentLight;
   float4            g_vEyeDir;   
};        
      
```



## <a name="initializing-interface-instances-in-an-application"></a>Инициализация экземпляров интерфейса в приложении

Экземпляры интерфейса инициализируются в коде приложения путем передачи динамического массива компоновки, содержащего назначения интерфейса, в один из методов [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) сетшадер.

Чтобы создать динамический массив компоновки, выполните следующие действия.

1.  Создайте объект компоновки класса с помощью [**креатекласслинкаже**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  Создайте шейдер, который будет использовать динамическое связывание классов, передав объект компоновки класса в качестве параметра функции создания шейдера.
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  Создайте объект [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) с помощью функции [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  Используйте объект отражения шейдера, чтобы получить количество экземпляров интерфейса в шейдере с помощью метода [**ID3D11ShaderReflection:: жетнуминтерфацеслотс**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  Создайте массив, достаточно большой для хранения числа экземпляров интерфейса в шейдере.
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  Определите индекс в массиве, соответствующий каждому экземпляру интерфейса, используя [**ID3D11ShaderReflection:: жетвариаблебинаме**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) и [**ID3D11ShaderReflectionVariable:: жетинтерфацеслот**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  Получите экземпляр класса для каждого объекта класса, производного от интерфейса в шейдере, с помощью [**ID3D11ClassLinkage:: жетклассинстанце**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  Установите для экземпляров интерфейса экземпляры класса, задав соответствующую запись в массиве динамической компоновки.
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  Передайте динамический массив компоновки в качестве параметра в вызов Сетшадер.
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a>См. также

[Динамическая компоновка](overviews-direct3d-11-hlsl-dynamic-linking.md)