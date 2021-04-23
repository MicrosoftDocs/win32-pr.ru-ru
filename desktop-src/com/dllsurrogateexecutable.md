---
title: дллсуррогатиксекутабле
description: Позволяет серверам DLL выполняться в пользовательском суррогатном процессе в сочетании со значением реестра Дллсуррогате. Если Дллсуррогатиксекутабле не указан, COM передает значение NULL в качестве значения первого параметра функции CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- COM-значение реестра Дллсуррогатиксекутабле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700955"
---
# <a name="dllsurrogateexecutable"></a><span data-ttu-id="31510-105">дллсуррогатиксекутабле</span><span class="sxs-lookup"><span data-stu-id="31510-105">DllSurrogateExecutable</span></span>

<span data-ttu-id="31510-106">Позволяет серверам DLL выполняться в пользовательском суррогатном процессе в сочетании со значением реестра [**дллсуррогате**](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="31510-106">Enables DLL servers to run in a custom surrogate process, in conjunction with the [**DllSurrogate**](dllsurrogate.md) registry value.</span></span> <span data-ttu-id="31510-107">Если **дллсуррогатиксекутабле** не указан, com передает значение **null** в качестве значения первого параметра функции [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="31510-107">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="31510-108">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="31510-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a><span data-ttu-id="31510-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31510-109">Remarks</span></span>

<span data-ttu-id="31510-110">Это значение имеет тип **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="31510-110">This value is of type **REG\_SZ**.</span></span> <span data-ttu-id="31510-111">Он работает в сочетании со значением [**дллсуррогате**](dllsurrogate.md) , чтобы предотвратить неоднозначность при использовании функции [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="31510-111">It works in conjunction with the [**DllSurrogate**](dllsurrogate.md) value to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="31510-112">**Дллсуррогате** указывает, нужно ли использовать пользовательский суррогат, и эти сведения передаются как первый параметр для **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="31510-112">**DllSurrogate** indicates whether a custom surrogate needs to be used, and this information is passed as the first parameter for **CreateProcess**.</span></span> <span data-ttu-id="31510-113">В зависимости от реализации **CreateProcess** эта информация может быть неоднозначной.</span><span class="sxs-lookup"><span data-stu-id="31510-113">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="31510-114">Если указан параметр **дллсуррогатиксекутабле** , com передает значение в качестве первого параметра **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="31510-114">If **DllSurrogateExecutable** is specified, COM passes the value as the first parameter of **CreateProcess**.</span></span> <span data-ttu-id="31510-115">Если **дллсуррогатиксекутабле** не указан, com передает значение **null** в качестве значения для первого параметра **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="31510-115">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31510-116">См. также</span><span class="sxs-lookup"><span data-stu-id="31510-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31510-117">**корегистерсуррогате**</span><span class="sxs-lookup"><span data-stu-id="31510-117">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="31510-118">Суррогаты библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="31510-118">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="31510-119">**дллсуррогате**</span><span class="sxs-lookup"><span data-stu-id="31510-119">**DllSurrogate**</span></span>](dllsurrogate.md)
</dt> <dt>

[<span data-ttu-id="31510-120">**исуррогате**</span><span class="sxs-lookup"><span data-stu-id="31510-120">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 