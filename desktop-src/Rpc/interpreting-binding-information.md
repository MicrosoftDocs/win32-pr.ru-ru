---
title: Анализ сведений о привязке
description: Microsoft RPC позволяет клиентским и серверным программам получать доступ к информации и интерпретировать ее в маркере привязки.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- Удаленный вызов процедур RPC, задачи, интерпретируемая привязка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487029"
---
# <a name="interpreting-binding-information"></a><span data-ttu-id="7c35b-104">Анализ сведений о привязке</span><span class="sxs-lookup"><span data-stu-id="7c35b-104">Interpreting Binding Information</span></span>

<span data-ttu-id="7c35b-105">Microsoft RPC позволяет клиентским и серверным программам получать доступ к информации и интерпретировать ее в маркере привязки.</span><span class="sxs-lookup"><span data-stu-id="7c35b-105">Microsoft RPC enables your client and server programs access to and interpret the information in a binding handle.</span></span> <span data-ttu-id="7c35b-106">Это не означает, что вы можете или попытаться напрямую обратиться к содержимому обработчика привязки.</span><span class="sxs-lookup"><span data-stu-id="7c35b-106">This does not mean that you can or should try to access the contents of a binding handle directly.</span></span> <span data-ttu-id="7c35b-107">Microsoft RPC предоставляет функции, которые задают и извлекают сведения в дескрипторах привязки.</span><span class="sxs-lookup"><span data-stu-id="7c35b-107">Microsoft RPC provides functions that set and retrieve the information in binding handles.</span></span>

<span data-ttu-id="7c35b-108">Чтобы получить сведения в маркере привязки, передайте этот обработчик в [**рпкбиндингтострингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="7c35b-108">To get the information in a binding handle, pass the handle to [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="7c35b-109">Он возвращает сведения о привязке в виде строки.</span><span class="sxs-lookup"><span data-stu-id="7c35b-109">It returns the binding information as a string.</span></span> <span data-ttu-id="7c35b-110">Для каждого вызова **рпкбиндингтострингбиндинг** необходимо иметь соответствующий вызов функции [**рпкстрингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span><span class="sxs-lookup"><span data-stu-id="7c35b-110">For every call to **RpcBindingToStringBinding**, you must have a corresponding call to the function [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span></span>

<span data-ttu-id="7c35b-111">Можно вызвать функцию [**рпкстрингбиндингпарсе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) для анализа строки, полученной из [**рпкбиндингтострингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="7c35b-111">You can call the function [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to parse the string you obtain from [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="7c35b-112">Эта функция выделяет строки, содержащие анализируемые данные.</span><span class="sxs-lookup"><span data-stu-id="7c35b-112">This function allocates strings to contain the information it parses.</span></span> <span data-ttu-id="7c35b-113">Если не нужно анализировать определенный фрагмент сведений о привязке, передайте значение **null** в качестве значения этого параметра.</span><span class="sxs-lookup"><span data-stu-id="7c35b-113">If you do not want it to parse a particular piece of binding information, pass a **NULL** as the value of that parameter.</span></span> <span data-ttu-id="7c35b-114">Обязательно вызывайте [**рпкстрингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) для каждой из строк, которые он выделяет.</span><span class="sxs-lookup"><span data-stu-id="7c35b-114">Be sure to call [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) for each of the strings it allocates.</span></span>

<span data-ttu-id="7c35b-115">В следующем фрагменте кода показано, как приложение может вызывать эти функции.</span><span class="sxs-lookup"><span data-stu-id="7c35b-115">The following code fragment illustrates how an application might call these functions.</span></span>


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



<span data-ttu-id="7c35b-116">Предыдущий пример кода вызывает функции [**рпкбиндингтострингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) и [**рпкстрингбиндингпарсе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) для получения и анализа информации в допустимом маркере привязки.</span><span class="sxs-lookup"><span data-stu-id="7c35b-116">The preceding sample code calls the functions [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) and [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to get and parse the information in a valid binding handle.</span></span> <span data-ttu-id="7c35b-117">Обратите внимание, что значение **null** было передано в качестве второго параметра для **рпкстрингбиндингпарсе**.</span><span class="sxs-lookup"><span data-stu-id="7c35b-117">Note that the value **NULL** was passed as the second parameter to **RpcStringBindingParse**.</span></span> <span data-ttu-id="7c35b-118">Это приводит к тому, что функция пропускает синтаксический анализ идентификатора UUID объекта.</span><span class="sxs-lookup"><span data-stu-id="7c35b-118">This causes that function to skip parsing the object UUID.</span></span> <span data-ttu-id="7c35b-119">Так как он не анализирует UUID, **рпкстрингбиндингпарсе** не будет выделять для него строку.</span><span class="sxs-lookup"><span data-stu-id="7c35b-119">Since it does not parse the UUID, **RpcStringBindingParse** will not allocate a string for it.</span></span> <span data-ttu-id="7c35b-120">Эта методика позволяет приложению выделить только память для сведений, которые необходимы для анализа и анализа.</span><span class="sxs-lookup"><span data-stu-id="7c35b-120">This technique enables your application to only allocate memory for the information you are interested in parsing and analyzing.</span></span>

 

 




