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
# <a name="interfaces-and-classes"></a><span data-ttu-id="3f735-103">Интерфейсы и классы</span><span class="sxs-lookup"><span data-stu-id="3f735-103">Interfaces and classes</span></span>

<span data-ttu-id="3f735-104">В компоновке динамического шейдера используются интерфейсы и классы высокого уровня шейдеров (HLSL), которые синтаксически похожи на их аналоги C++.</span><span class="sxs-lookup"><span data-stu-id="3f735-104">Dynamic shader linkage makes use of high-level shader language (HLSL) interfaces and classes that are syntactically similar to their C++ counterparts.</span></span> <span data-ttu-id="3f735-105">Это позволяет шейдеру ссылаться на абстрактные экземпляры интерфейса во время компиляции и оставлять эти экземпляры конкретным классам для приложения в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="3f735-105">This allows shaders to reference abstract interface instances at compile time and leave resolution of those instances to concrete classes for the application at runtime.</span></span>

<span data-ttu-id="3f735-106">В следующих разделах подробно описано, как настроить шейдер для использования интерфейсов и классов, а также как инициализировать экземпляры интерфейса в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="3f735-106">The following sections detail how to setup a shader to use interfaces and classes and how to initialize interface instances in application code.</span></span>

-   [<span data-ttu-id="3f735-107">Объявление интерфейсов</span><span class="sxs-lookup"><span data-stu-id="3f735-107">Declaring Interfaces</span></span>](#declaring-interfaces)
-   [<span data-ttu-id="3f735-108">Объявление классов</span><span class="sxs-lookup"><span data-stu-id="3f735-108">Declaring Classes</span></span>](#declaring-classes)
-   [<span data-ttu-id="3f735-109">Объявления экземпляров интерфейса в шейдере</span><span class="sxs-lookup"><span data-stu-id="3f735-109">Interface Instance Declarations in a Shader</span></span>](#interface-instance-declarations-in-a-shader)
-   [<span data-ttu-id="3f735-110">Объявления экземпляров классов в шейдере</span><span class="sxs-lookup"><span data-stu-id="3f735-110">Class Instance Declarations in a Shader</span></span>](#class-instance-declarations-in-a-shader)
-   [<span data-ttu-id="3f735-111">Инициализация экземпляров интерфейса в приложении</span><span class="sxs-lookup"><span data-stu-id="3f735-111">Initializing Interface Instances in an Application</span></span>](#initializing-interface-instances-in-an-application)
-   [<span data-ttu-id="3f735-112">См. также</span><span class="sxs-lookup"><span data-stu-id="3f735-112">Related topics</span></span>](#related-topics)

## <a name="declaring-interfaces"></a><span data-ttu-id="3f735-113">Объявление интерфейсов</span><span class="sxs-lookup"><span data-stu-id="3f735-113">Declaring interfaces</span></span>

<span data-ttu-id="3f735-114">Интерфейс функционирует аналогичным образом для абстрактного базового класса в C++.</span><span class="sxs-lookup"><span data-stu-id="3f735-114">An interface functions in a similar manner to an abstract base class in C++.</span></span> <span data-ttu-id="3f735-115">Интерфейс объявляется в шейдере с помощью ключевого слова Interface и содержит только объявления методов.</span><span class="sxs-lookup"><span data-stu-id="3f735-115">An interface is declared in a shader using the interface keyword and only contains method declarations.</span></span> <span data-ttu-id="3f735-116">Методы, объявленные в интерфейсе, будут виртуальными методами в любых классах, производных от интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3f735-116">The methods declared in an interface will all be virtual methods in any classes derived from the interface.</span></span> <span data-ttu-id="3f735-117">Производные классы должны реализовывать все методы, объявленные в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="3f735-117">Derived classes must implement all methods declared in an interface.</span></span> <span data-ttu-id="3f735-118">Обратите внимание, что интерфейсы являются единственным способом объявления виртуальных методов, в C++ нет виртуального ключевого слова, а классы Коннот объявляют виртуальные методы.</span><span class="sxs-lookup"><span data-stu-id="3f735-118">Note that interfaces are the only way to declare virtual methods, there is no virtual keyword as in C++, and classes connot declare virtual methods.</span></span>

<span data-ttu-id="3f735-119">В следующем примере кода шейдера объявляются два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3f735-119">The following example shader code declares two interfaces.</span></span>


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



## <a name="declaring-classes"></a><span data-ttu-id="3f735-120">Объявление классов</span><span class="sxs-lookup"><span data-stu-id="3f735-120">Declaring Classes</span></span>

<span data-ttu-id="3f735-121">Класс ведет себя аналогичным образом для классов в C++.</span><span class="sxs-lookup"><span data-stu-id="3f735-121">A class behaves in a similar manner to classes in C++.</span></span> <span data-ttu-id="3f735-122">Класс объявляется с ключевым словом class и может содержать переменные-члены и методы.</span><span class="sxs-lookup"><span data-stu-id="3f735-122">A class is declared with the class keyword and can contain member variables and methods.</span></span> <span data-ttu-id="3f735-123">Класс может наследовать от нуля или от одного класса и от нуля или нескольких интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="3f735-123">A class can inherit from zero or one class and zero or more interfaces.</span></span> <span data-ttu-id="3f735-124">Классы должны реализовывать или наследовать реализации для всех интерфейсов в цепочке наследования, а также создавать экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="3f735-124">Classes must implement or inherit implementations for all interfaces in its inheritance chain or the class cannot be instantiated.</span></span>

<span data-ttu-id="3f735-125">Следующий пример кода шейдера иллюстрирует создание производного класса от интерфейса и от другого класса.</span><span class="sxs-lookup"><span data-stu-id="3f735-125">The following example shader code illustrates deriving a class from an interface and from another class.</span></span>


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



## <a name="interface-instance-declarations-in-a-shader"></a><span data-ttu-id="3f735-126">Объявления экземпляров интерфейса в шейдере</span><span class="sxs-lookup"><span data-stu-id="3f735-126">Interface Instance Declarations in a Shader</span></span>

<span data-ttu-id="3f735-127">Экземпляр интерфейса выступает в качестве заполнителя для экземпляров класса, предоставляющих реализацию методов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3f735-127">An interface instance acts as a place holder for class instances that provide an implementation of the interface's methods.</span></span> <span data-ttu-id="3f735-128">Использование экземпляра интерфейса позволяет коду шейдера вызывать метод, не зная, какая реализация этого метода будет вызываться.</span><span class="sxs-lookup"><span data-stu-id="3f735-128">Using an instance of an interface allows shader code to call a method without knowing which implementation of that method will be invoked.</span></span> <span data-ttu-id="3f735-129">Код шейдера объявляет один или несколько экземпляров для каждого определяемого им интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3f735-129">Shader code declares one or more instances for each interface it defines.</span></span> <span data-ttu-id="3f735-130">Эти экземпляры используются в коде шейдера аналогичным образом для указателей базовых классов C++.</span><span class="sxs-lookup"><span data-stu-id="3f735-130">These instances are used in shader code in a similar manner to C++ base class pointers.</span></span>

<span data-ttu-id="3f735-131">В следующем примере кода шейдера показано объявление нескольких экземпляров интерфейса и их использование в коде шейдера.</span><span class="sxs-lookup"><span data-stu-id="3f735-131">The following example shader code illustrates declaring several interface instances and using them in shader code.</span></span>


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



## <a name="class-instance-declarations-in-a-shader"></a><span data-ttu-id="3f735-132">Объявления экземпляров классов в шейдере</span><span class="sxs-lookup"><span data-stu-id="3f735-132">Class Instance Declarations in a Shader</span></span>

<span data-ttu-id="3f735-133">Каждый класс, который будет использоваться вместо экземпляра интерфейса, должен быть либо объявлен как переменная в буфере констант, либо создан приложением во время выполнения с помощью метода [**ID3D11ClassLinkage:: креатеклассинстанце**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) .</span><span class="sxs-lookup"><span data-stu-id="3f735-133">Each class that will be used in place of an interface instance must either be declared as a variable in a constant buffer or created by the application at runtime using the [**ID3D11ClassLinkage::CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) method.</span></span> <span data-ttu-id="3f735-134">Экземпляры интерфейса будут указываться в экземплярах класса в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="3f735-134">Interface instances will be pointed at class instances in the application code.</span></span> <span data-ttu-id="3f735-135">На экземпляры классов можно ссылаться в коде шейдера, как и любую другую переменную, но класс, производный от интерфейса, обычно используется только с экземпляром интерфейса и не будет ссылаться непосредственно на код шейдера.</span><span class="sxs-lookup"><span data-stu-id="3f735-135">Class instances can be referenced in shader code like any other variable, but a class that is derived from an interface will typically only be used with an interface instance and will not be referenced by shader code directly.</span></span>

<span data-ttu-id="3f735-136">В следующем примере кода шейдера показано объявление нескольких экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="3f735-136">The following example shader code illustrates declaring several class instances.</span></span>


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



## <a name="initializing-interface-instances-in-an-application"></a><span data-ttu-id="3f735-137">Инициализация экземпляров интерфейса в приложении</span><span class="sxs-lookup"><span data-stu-id="3f735-137">Initializing Interface Instances in an Application</span></span>

<span data-ttu-id="3f735-138">Экземпляры интерфейса инициализируются в коде приложения путем передачи динамического массива компоновки, содержащего назначения интерфейса, в один из методов [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) сетшадер.</span><span class="sxs-lookup"><span data-stu-id="3f735-138">Interface instances are initialized in application code by passing a dynamic linkage array containing interface assignments to one of the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader methods.</span></span>

<span data-ttu-id="3f735-139">Чтобы создать динамический массив компоновки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f735-139">To create a dynamic linkage array use the following steps</span></span>

1.  <span data-ttu-id="3f735-140">Создайте объект компоновки класса с помощью [**креатекласслинкаже**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span><span class="sxs-lookup"><span data-stu-id="3f735-140">Create a class linkage object using [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span></span>
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  <span data-ttu-id="3f735-141">Создайте шейдер, который будет использовать динамическое связывание классов, передав объект компоновки класса в качестве параметра функции создания шейдера.</span><span class="sxs-lookup"><span data-stu-id="3f735-141">Create the shader that will be using dynamic class linking, passing the class linkage object as a parameter to the shader's create function.</span></span>
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  <span data-ttu-id="3f735-142">Создайте объект [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) с помощью функции [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="3f735-142">Create a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) object using the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) function.</span></span>
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  <span data-ttu-id="3f735-143">Используйте объект отражения шейдера, чтобы получить количество экземпляров интерфейса в шейдере с помощью метода [**ID3D11ShaderReflection:: жетнуминтерфацеслотс**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .</span><span class="sxs-lookup"><span data-stu-id="3f735-143">Use the shader reflection object to get the number of interface instances in the shader using the [**ID3D11ShaderReflection::GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) method.</span></span>
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  <span data-ttu-id="3f735-144">Создайте массив, достаточно большой для хранения числа экземпляров интерфейса в шейдере.</span><span class="sxs-lookup"><span data-stu-id="3f735-144">Create an array large enough to hold the number of interface instances in the shader.</span></span>
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  <span data-ttu-id="3f735-145">Определите индекс в массиве, соответствующий каждому экземпляру интерфейса, используя [**ID3D11ShaderReflection:: жетвариаблебинаме**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) и [**ID3D11ShaderReflectionVariable:: жетинтерфацеслот**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span><span class="sxs-lookup"><span data-stu-id="3f735-145">Determine the index in the array that corresponds to each interface instance using [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) and [**ID3D11ShaderReflectionVariable::GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span></span>
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  <span data-ttu-id="3f735-146">Получите экземпляр класса для каждого объекта класса, производного от интерфейса в шейдере, с помощью [**ID3D11ClassLinkage:: жетклассинстанце**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span><span class="sxs-lookup"><span data-stu-id="3f735-146">Get a class instance for each class object derived from an interface in the shader using [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span></span>
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  <span data-ttu-id="3f735-147">Установите для экземпляров интерфейса экземпляры класса, задав соответствующую запись в массиве динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="3f735-147">Set interface instances to class instances by setting the corresponding entry in the dynamic linkage array.</span></span>
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  <span data-ttu-id="3f735-148">Передайте динамический массив компоновки в качестве параметра в вызов Сетшадер.</span><span class="sxs-lookup"><span data-stu-id="3f735-148">Pass the dynamic linkage array as a parameter to a SetShader call.</span></span>
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a><span data-ttu-id="3f735-149">См. также</span><span class="sxs-lookup"><span data-stu-id="3f735-149">Related topics</span></span>

[<span data-ttu-id="3f735-150">Динамическая компоновка</span><span class="sxs-lookup"><span data-stu-id="3f735-150">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)