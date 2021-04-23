---
title: msc_ver Switch
description: Параметр/МСК \_ ver позволяет использовать MIDL для создания кода, который включает оптимизацию для различных версий компиляторов Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver параметр MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889780"
---
# <a name="msc_ver-switch"></a><span data-ttu-id="0343e-104">\_коммутатор/МСК ver</span><span class="sxs-lookup"><span data-stu-id="0343e-104">/msc\_ver switch</span></span>

<span data-ttu-id="0343e-105">Параметр **/МСК \_ ver** позволяет использовать MIDL для создания кода, который включает оптимизацию для различных версий компиляторов Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="0343e-105">The **/msc\_ver** switch is used to allow MIDL to generate code that includes optimizations for different versions of Microsoft C/C++ compilers.</span></span>

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a><span data-ttu-id="0343e-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="0343e-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="0343e-107">*\_номер версии*</span><span class="sxs-lookup"><span data-stu-id="0343e-107">*version\_number*</span></span> 
</dt> <dd>

<span data-ttu-id="0343e-108">Указывает целочисленный номер версии компилятора Microsoft Visual C++, который будет использоваться для компиляции заглушек клиента и сервера распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="0343e-108">Specifies an integer version number of the Microsoft Visual C++ compiler that will be used to compile the client and server stubs of the distributed application.</span></span> <span data-ttu-id="0343e-109">Номер версии по умолчанию — 1100, соответствующий версии Visual C++ 5,0.</span><span class="sxs-lookup"><span data-stu-id="0343e-109">The default version number is 1100, which corresponds to Visual C++ version 5.0.</span></span> <span data-ttu-id="0343e-110">Номер версии 1200 соответствует Visual C++ версии 6,0 и т. д.</span><span class="sxs-lookup"><span data-stu-id="0343e-110">The version number 1200 corresponds to Visual C++ version 6.0, and so on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0343e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0343e-111">Remarks</span></span>

<span data-ttu-id="0343e-112">В частности, значения версии 1100 или выше приводят к тому, что компилятор MIDL создает код, использующий директиву **\_ \_ declspec (UUID ())** .</span><span class="sxs-lookup"><span data-stu-id="0343e-112">In particular, version values of 1100 or greater cause the MIDL compiler to generate code utilizing the **\_\_declspec(uuid())** directive.</span></span> <span data-ttu-id="0343e-113">Он также активирует макросы, использующие директивы **\_ \_ declspec (selectany)** и **\_ \_ declspec (vtable)** .</span><span class="sxs-lookup"><span data-stu-id="0343e-113">It also activates macros that use the **\_\_declspec(selectany)** and **\_\_declspec(novtable)** directives.</span></span>

 

 




