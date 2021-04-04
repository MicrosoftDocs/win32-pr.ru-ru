---
title: Атрибут disable_consistency_check
description: Направляет RPC, чтобы не применять проверку согласованности корреляции.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329048"
---
# <a name="disable_consistency_check-attribute"></a><span data-ttu-id="6d5f0-103">отключить \_ \_ атрибут проверки согласованности</span><span class="sxs-lookup"><span data-stu-id="6d5f0-103">disable\_consistency\_check Attribute</span></span>

<span data-ttu-id="6d5f0-104">Направляет RPC, чтобы не применять проверку согласованности корреляции.</span><span class="sxs-lookup"><span data-stu-id="6d5f0-104">Directs RPC to not enforce correlation consistency checking.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

<span data-ttu-id="6d5f0-105">Для коррелированных параметров RPC будет обеспечивать передачу буфера, отличного от NULL, если значение переменной счетчика корреляций не равно null.</span><span class="sxs-lookup"><span data-stu-id="6d5f0-105">For correlated parameters, RPC will enforce that a non-null buffer is passed when the correlation count variable is non-null.</span></span>

## <a name="example"></a><span data-ttu-id="6d5f0-106">Пример</span><span class="sxs-lookup"><span data-stu-id="6d5f0-106">Example</span></span>

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

<span data-ttu-id="6d5f0-107">Если параметр *MyString* имеет **значение NULL**, то RPC отклонит вызов, если для параметра length задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="6d5f0-107">If *MyString* is **NULL**, RPC will reject the call unless Length is set to 0.</span></span> <span data-ttu-id="6d5f0-108">Обратите внимание, что RPC допускает *длину* 0, в то время как *MyString* не имеет значение null, а RPC будет обрабатывать *MyString* как выделение буфера нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="6d5f0-108">Note that RPC will allow *Length* to be 0 while *MyString* is non-NULL, and RPC will treat *MyString* as a 0-length buffer allocation.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d5f0-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d5f0-109">Remarks</span></span>

<span data-ttu-id="6d5f0-110">Чтобы отключить эту проверку, IDL может содержать атрибут " \[ Отключить \_ проверку согласованности" \_ \] для параметра, typedef или типа указателя.</span><span class="sxs-lookup"><span data-stu-id="6d5f0-110">To disable this checking, the IDL can contain the \[disable\_consistency\_check\] attribute on a parameter, typedef, or pointer type.</span></span> <span data-ttu-id="6d5f0-111">Это позволит RPC не обеспечивать согласованность между указателем буфера и переменной корреляции для буфера, на который указывает параметр или указатель.</span><span class="sxs-lookup"><span data-stu-id="6d5f0-111">This will direct RPC to not enforce the consistency between the buffer pointer and the correlation variable for the buffer pointed to by the parameter or pointer.</span></span>

<span data-ttu-id="6d5f0-112">Чтобы отключить проверку согласованности для всей компиляции MIDL (и отключить принудительную проверку во всех случаях), можно использовать параметр командной строки MIDL [/бакквард \_ совместимого майбенулл \_ размера](-backward-compat.md) .</span><span class="sxs-lookup"><span data-stu-id="6d5f0-112">To disable consistency checking for an entire MIDL compilation (and disable enforcement of the checking in all cases), the MIDL command line switch [/backward\_compat maybenull\_sizeis](-backward-compat.md) can be used.</span></span> <span data-ttu-id="6d5f0-113">Для этого необходимо, чтобы целевой объект компиляции MIDL был не меньше "Target NT60".</span><span class="sxs-lookup"><span data-stu-id="6d5f0-113">This requires that the target of the MIDL compilation be at least â€“target NT60.</span></span>

 

 




