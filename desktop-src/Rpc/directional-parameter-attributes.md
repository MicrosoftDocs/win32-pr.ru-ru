---
title: Атрибуты направления (параметра)
description: Атрибуты направления описывают, передаются ли данные с клиента на сервер, с сервера на клиент или в оба этих атрибута.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- Удаленный вызов процедур RPC, описание, атрибуты направления
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134223"
---
# <a name="directional-parameter-attributes"></a><span data-ttu-id="b4d9c-106">Атрибуты направления (параметра)</span><span class="sxs-lookup"><span data-stu-id="b4d9c-106">Directional (Parameter) Attributes</span></span>

<span data-ttu-id="b4d9c-107">Атрибуты направления описывают, передаются ли данные с клиента на сервер, с сервера на клиент или в оба этих атрибута.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-107">Directional attributes describe whether the data is transmitted from client to server, server to client, or both.</span></span> <span data-ttu-id="b4d9c-108">Все параметры в прототипе функции должны быть связаны с атрибутами направления.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-108">All parameters in the function prototype must be associated with directional attributes.</span></span> <span data-ttu-id="b4d9c-109">Три возможных сочетания атрибутов направления: 1) \[ [**в**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] и 3) \[ **в**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="b4d9c-109">The three possible combinations of directional attributes are: 1) \[[**in**](/windows/desktop/Midl/in)\], 2) \[[**out**](/windows/desktop/Midl/out-idl)\], and 3) \[**in**, **out**\].</span></span> <span data-ttu-id="b4d9c-110">Они описывают способ передачи параметров между вызовом и вызовом процедур.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-110">These describe the way parameters are passed between calling and called procedures.</span></span> <span data-ttu-id="b4d9c-111">При компиляции в режиме по умолчанию (расширенный режим Майкрософт) и пропущении атрибута направления для параметра компилятор MIDL предполагает, что значение по умолчанию — \[ **в** \] .</span><span class="sxs-lookup"><span data-stu-id="b4d9c-111">When you compile in the default (Microsoft-extended mode) and you omit a directional attribute for a parameter, the MIDL compiler assumes a default value of \[**in**\].</span></span>

<span data-ttu-id="b4d9c-112">\[ [**Выходной**](/windows/desktop/Midl/out-idl) \] параметр должен быть указателем.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-112">An \[[**out**](/windows/desktop/Midl/out-idl)\] parameter must be a pointer.</span></span> <span data-ttu-id="b4d9c-113">Фактически \[  \] атрибут out не имеет смысла при применении к параметрам, которые не являются указателями, так как параметры функции C передаются по значению.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-113">In fact, the \[**out**\] attribute is not meaningful when applied to parameters that do not act as pointers because C function parameters are passed by value.</span></span> <span data-ttu-id="b4d9c-114">В C вызываемая функция получает закрытую копию значения параметра; Он не может изменить значение вызывающей функции для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-114">In C, the called function receives a private copy of the parameter value; it cannot change the calling function's value for that parameter.</span></span> <span data-ttu-id="b4d9c-115">Однако если параметр выступает в качестве указателя, его можно использовать для доступа к памяти и его изменения.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-115">If the parameter acts as a pointer, however, it can be used to access and modify memory.</span></span> <span data-ttu-id="b4d9c-116">Атрибут \[ **out** \] указывает, что серверная функция должна возвращать значение вызывающей функции клиента, и эта память, связанная с указателем, должна возвращаться в соответствии с атрибутами, назначенными указателю.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-116">The \[**out**\] attribute indicates that the server function should return the value to the client's calling function, and that memory associated with the pointer should be returned in accordance with the attributes assigned to the pointer.</span></span>

<span data-ttu-id="b4d9c-117">В следующем интерфейсе показаны три возможных сочетания атрибутов направления, которые можно применить к параметру.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-117">The following interface demonstrates the three possible combinations of directional attributes that can be applied to a parameter.</span></span> <span data-ttu-id="b4d9c-118">Функция **инаутпрок** ОПРЕДЕЛЯЕТСЯ в IDL-файле следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b4d9c-118">The function **InOutProc** is defined in the IDL file as:</span></span>

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

<span data-ttu-id="b4d9c-119">Первый параметр *S1* используется \[ [](/windows/desktop/Midl/in) \] только в.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-119">The first parameter, *s1*, is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="b4d9c-120">Его значение передается на удаленный компьютер, но не возвращается вызывающей процедуре.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-120">Its value is transmitted to the remote computer, but is not returned to the calling procedure.</span></span> <span data-ttu-id="b4d9c-121">Несмотря на то, что серверное приложение может изменить значение *S1*, значение *S1* на клиенте будет таким же, как и после вызова.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-121">Although the server application can change its value for *s1*, the value of *s1* on the client is the same before and after the call.</span></span>

<span data-ttu-id="b4d9c-122">Второй параметр, *PS2*, определен в прототипе функции как указатель с \[ [](/windows/desktop/Midl/in) \] атрибутами in и \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="b4d9c-122">The second parameter, *ps2*, is defined in the function prototype as a pointer with both \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] attributes.</span></span> <span data-ttu-id="b4d9c-123">Атрибут \[ **in** \] указывает, что значение параметра передается с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-123">The \[**in**\] attribute indicates that the value of the parameter is passed from the client to the server.</span></span> <span data-ttu-id="b4d9c-124">Атрибут \[ **out** \] указывает, что значение, на которое указывает *PS2* , возвращается клиенту.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-124">The \[**out**\] attribute indicates that the value pointed to by *ps2* is returned to the client.</span></span>

<span data-ttu-id="b4d9c-125">Третий параметр — только \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="b4d9c-125">The third parameter is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="b4d9c-126">Для параметра на сервере выделено место, но при входе значение не определено.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-126">Space is allocated for the parameter on the server, but the value is undefined on entry.</span></span> <span data-ttu-id="b4d9c-127">Как упоминалось выше, все \[ **выходные** \] параметры должны быть указателями.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-127">As mentioned above, all \[**out**\] parameters must be pointers.</span></span>

<span data-ttu-id="b4d9c-128">Удаленная процедура изменяет значение всех трех параметров, но клиенту доступны только новые значения \[ параметров [**out**](/windows/desktop/Midl/out-idl) \] и \[ [**in**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="b4d9c-128">The remote procedure changes the value of all three parameters, but only the new values of the \[[**out**](/windows/desktop/Midl/out-idl)\] and \[[**in**](/windows/desktop/Midl/in)\] parameters are available to the client.</span></span>


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



<span data-ttu-id="b4d9c-129">При возврате из вызова **инаутпрок** изменяется второй и третий параметры.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-129">On return from the call to **InOutProc**, the second and third parameters are modified.</span></span> <span data-ttu-id="b4d9c-130">Первый параметр, который находится \[ [**в только в**](/windows/desktop/Midl/in) \] , не изменен.</span><span class="sxs-lookup"><span data-stu-id="b4d9c-130">The first parameter, which is \[[**in**](/windows/desktop/Midl/in)\] only, is unchanged.</span></span>

![параметры In](images/prog-a22.png)

![параметры вывода](images/prog-a23.png)

![параметры out](images/prog-a21.png)

 

 