---
title: ключевое слово UNION (RPC)
description: Для объединения требуются специальные ключевые слова MIDL для поддержки их использования с удаленным вызовом процедур (RPC).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337617"
---
# <a name="union-keyword-rpc"></a><span data-ttu-id="5ff44-103">ключевое слово UNION (RPC)</span><span class="sxs-lookup"><span data-stu-id="5ff44-103">union keyword (RPC)</span></span>

<span data-ttu-id="5ff44-104">Некоторые функции языка C, такие как объединения, занимают специальные ключевые слова MIDL для поддержки их использования в удаленных вызовах процедур.</span><span class="sxs-lookup"><span data-stu-id="5ff44-104">Some features of the C language, such as unions, require special MIDL keywords to support their use in remote procedure calls.</span></span> <span data-ttu-id="5ff44-105">Объединение в языке C представляет собой переменную, которая содержит объекты различных типов и размеров.</span><span class="sxs-lookup"><span data-stu-id="5ff44-105">A union in the C language is a variable that holds objects of different types and sizes.</span></span> <span data-ttu-id="5ff44-106">Разработчик обычно создает переменную для наблюдения за типами, хранящимися в объединении.</span><span class="sxs-lookup"><span data-stu-id="5ff44-106">The developer usually creates a variable to keep track of the types stored in the union.</span></span> <span data-ttu-id="5ff44-107">Для правильной работы в распределенной среде переменная, указывающая тип объединения или *discriminant*, также должна быть доступна удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="5ff44-107">To operate correctly in a distributed environment, the variable that indicates the type of the union, or the *discriminant*, must also be available to the remote computer.</span></span> <span data-ttu-id="5ff44-108">MIDL предоставляет \[ [**\_ тип параметра**](/windows/desktop/Midl/switch-type) \] и \[ [**параметр \_ —**](/windows/desktop/Midl/switch-is) \] Ключевые слова для задания типа и имени discriminant.</span><span class="sxs-lookup"><span data-stu-id="5ff44-108">MIDL provides the \[[**switch\_type**](/windows/desktop/Midl/switch-type)\] and \[[**switch\_is**](/windows/desktop/Midl/switch-is)\] keywords to identify the discriminant type and name.</span></span>

<span data-ttu-id="5ff44-109">MIDL требует, чтобы discriminant передавался вместе с объединением одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="5ff44-109">MIDL requires that the discriminant be transmitted with the union in one of two ways:</span></span>

-   <span data-ttu-id="5ff44-110">Union и discriminant должны быть указаны в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="5ff44-110">The union and the discriminant must be provided as parameters.</span></span>
-   <span data-ttu-id="5ff44-111">Объединение и discriminant должны быть упакованы в структуру.</span><span class="sxs-lookup"><span data-stu-id="5ff44-111">The union and the discriminant must be packaged in a structure.</span></span>

<span data-ttu-id="5ff44-112">Два фундаментальных типа размеченных объединений предоставляются MIDL: [**неинкапсулированное \_ объединение**](/windows/desktop/Midl/nonencapsulated-unions) и [**инкапсулированное \_ объединение**](/windows/desktop/Midl/encapsulated-unions).</span><span class="sxs-lookup"><span data-stu-id="5ff44-112">Two fundamental types of discriminated unions are provided by MIDL: [**nonencapsulated\_union**](/windows/desktop/Midl/nonencapsulated-unions) and [**encapsulated\_union**](/windows/desktop/Midl/encapsulated-unions).</span></span> <span data-ttu-id="5ff44-113">Discriminant неинкапсулированного объединения является другим параметром, если объединение является параметром.</span><span class="sxs-lookup"><span data-stu-id="5ff44-113">The discriminant of a nonencapsulated union is another parameter if the union is a parameter.</span></span> <span data-ttu-id="5ff44-114">Это еще одно поле, если объединение является полем структуры.</span><span class="sxs-lookup"><span data-stu-id="5ff44-114">It is another field if the union is a field of a structure.</span></span> <span data-ttu-id="5ff44-115">Определение инкапсулированного объединения преобразуется в определение структуры, первым полем которого является discriminant, а второе и Последнее поля — объединение.</span><span class="sxs-lookup"><span data-stu-id="5ff44-115">The definition of an encapsulated union is turned into a structure definition whose first field is the discriminant and whose second and last fields are the union.</span></span> <span data-ttu-id="5ff44-116">В следующем примере показано, как указать параметры Union и discriminant в качестве параметров:</span><span class="sxs-lookup"><span data-stu-id="5ff44-116">The following example demonstrates how to provide the union and discriminant as parameters:</span></span>

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

<span data-ttu-id="5ff44-117">Объединение в предыдущем примере может содержать одно значение: **Short**, **float** или **char**.</span><span class="sxs-lookup"><span data-stu-id="5ff44-117">The union in the preceding example can contain a single value: either **short**, **float**, or **char**.</span></span> <span data-ttu-id="5ff44-118">Определение типа для объединения включает в себя атрибут **\_ типа параметра** MIDL, указывающий тип discriminant.</span><span class="sxs-lookup"><span data-stu-id="5ff44-118">The type definition for the union includes the MIDL **switch\_type** attribute that specifies the type of the discriminant.</span></span> <span data-ttu-id="5ff44-119">Здесь \[ тип параметра \_ (Short) \] указывает, что discriminant имеет тип **Short**.</span><span class="sxs-lookup"><span data-stu-id="5ff44-119">Here, \[switch\_type(short)\] specifies that the discriminant is of type **short**.</span></span> <span data-ttu-id="5ff44-120">Параметр должен быть целочисленным типом.</span><span class="sxs-lookup"><span data-stu-id="5ff44-120">The switch must be an integer type.</span></span>

<span data-ttu-id="5ff44-121">Если объединение является членом структуры, то discriminant должен быть членом той же структуры.</span><span class="sxs-lookup"><span data-stu-id="5ff44-121">If the union is a member of a structure, then the discriminant must be a member of the same structure.</span></span> <span data-ttu-id="5ff44-122">Если Union является параметром, discriminant должен быть другим параметром.</span><span class="sxs-lookup"><span data-stu-id="5ff44-122">If the union is a parameter, then the discriminant must be another parameter.</span></span> <span data-ttu-id="5ff44-123">Прототип для функции **унионпарампрок** в предыдущем примере показывает discriminant *сутипе* в качестве последнего параметра вызова.</span><span class="sxs-lookup"><span data-stu-id="5ff44-123">The prototype for the function **UnionParamProc** in the preceding example shows the discriminant *sUtype* as the last parameter of the call.</span></span> <span data-ttu-id="5ff44-124">(Discriminant может находиться в любом месте вызова.) Тип параметра, указанного в **\[ \_ \] параметре, должен** соответствовать типу, указанному в атрибуте **\[ \_ типа \] переключателя** .</span><span class="sxs-lookup"><span data-stu-id="5ff44-124">(The discriminant can appear in any position in the call.) The type of the parameter specified in the **\[switch\_is\]** attribute must match the type specified in the **\[switch\_type\]** attribute.</span></span>

<span data-ttu-id="5ff44-125">В следующем примере демонстрируется использование одной структуры, которая упаковывает discriminant с объединением:</span><span class="sxs-lookup"><span data-stu-id="5ff44-125">The following example demonstrates the use of a single structure that packages the discriminant with the union:</span></span>

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

<span data-ttu-id="5ff44-126">Компилятор Microsoft RPC MIDL позволяет объявлять Union за пределами конструкций [**typedef**](/windows/desktop/Midl/typedef) .</span><span class="sxs-lookup"><span data-stu-id="5ff44-126">The Microsoft RPC MIDL compiler allows union declarations outside of [**typedef**](/windows/desktop/Midl/typedef) constructs.</span></span> <span data-ttu-id="5ff44-127">Эта функция является расширением для устройства DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="5ff44-127">This feature is an extension to DCE IDL.</span></span> <span data-ttu-id="5ff44-128">Дополнительные сведения см. в разделе [**Union**](/windows/desktop/Midl/union).</span><span class="sxs-lookup"><span data-stu-id="5ff44-128">For more information, see [**union**](/windows/desktop/Midl/union).</span></span>

 

 