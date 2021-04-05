---
title: Требования к серверу DLL
description: Хотя большинство библиотек DLL могут работать в суррогате, некоторые библиотеки DLL не могут.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068628"
---
# <a name="dll-server-requirements"></a><span data-ttu-id="00e58-103">Требования к серверу DLL</span><span class="sxs-lookup"><span data-stu-id="00e58-103">DLL Server Requirements</span></span>

<span data-ttu-id="00e58-104">Хотя большинство библиотек DLL могут работать в суррогате, некоторые библиотеки DLL не могут.</span><span class="sxs-lookup"><span data-stu-id="00e58-104">While most DLLs can run in a surrogate, some DLLs cannot.</span></span>

<span data-ttu-id="00e58-105">Библиотека DLL должна быть правильно настроена, если вы хотите использовать заданный системой суррогат.</span><span class="sxs-lookup"><span data-stu-id="00e58-105">The DLL must be well-behaved if you want to use the system-supplied surrogate.</span></span> <span data-ttu-id="00e58-106">Например, Библиотека DLL, которая вызывает методы, которые регистрируют обратные вызовы от клиента, попытается вызвать эти обратные вызовы, как если бы полученные указатели функций были инструкциями в адресном пространстве, что не так.</span><span class="sxs-lookup"><span data-stu-id="00e58-106">For example, a DLL that calls methods that register callbacks from the client would try to invoke those callbacks as if the function pointers it received were for instructions in its address space, which is not the case.</span></span> <span data-ttu-id="00e58-107">Аналогичным образом, Библиотека DLL, использующая глобальную переменную, которая не требует доступа к клиенту, не будет работать.</span><span class="sxs-lookup"><span data-stu-id="00e58-107">Similarly, a DLL that uses a global variable that it expects the client to access would not work.</span></span> <span data-ttu-id="00e58-108">В общем случае параметры, которые не могут быть правильно упакованы, не позволяют серверу DLL выполняться вне клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="00e58-108">In general, parameters that cannot be properly marshaled will prevent the DLL server from running outside the client process.</span></span> <span data-ttu-id="00e58-109">Во многих случаях можно написать специальный суррогат, специально разработанный для компенсации «плохого» поведения.</span><span class="sxs-lookup"><span data-stu-id="00e58-109">In many cases, you can write a custom surrogate specifically designed to compensate for "bad" behavior.</span></span> <span data-ttu-id="00e58-110">(Дополнительные сведения см. [в разделе Написание пользовательского суррогата](writing-a-custom-surrogate.md).)</span><span class="sxs-lookup"><span data-stu-id="00e58-110">(For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).)</span></span>

<span data-ttu-id="00e58-111">Если сервер DLL использует пользовательские интерфейсы, необходимо убедиться, что код для маршалирования доступен для этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="00e58-111">If the DLL server uses custom interfaces, you would have to ensure that marshaling code is available for those interfaces.</span></span> <span data-ttu-id="00e58-112">Например, можно создать и зарегистрировать прокси-библиотеку DLL или предоставить и зарегистрировать библиотеку типов, которая позволит серверу правильно работать при выполнении в суррогате.</span><span class="sxs-lookup"><span data-stu-id="00e58-112">For example, you could build and register a proxy DLL or provide and register a type library that would allow the server to function correctly while running in a surrogate.</span></span>

<span data-ttu-id="00e58-113">Серверы DLL будут загружены только в суррогатный процесс, выполняемый в правильном контексте безопасности.</span><span class="sxs-lookup"><span data-stu-id="00e58-113">DLL servers will be loaded only into a surrogate process running in the proper security context.</span></span> <span data-ttu-id="00e58-114">Контекст безопасности для суррогата сервера DLL определяется так же, как и для серверов EXE.</span><span class="sxs-lookup"><span data-stu-id="00e58-114">The security context for the DLL server surrogate is determined in the same way as for EXE servers.</span></span> <span data-ttu-id="00e58-115">Суррогат сервера DLL выполняется в том же контексте безопасности, что и клиент, за исключением случаев, когда значение **runas** , определяющее контекст безопасности, задается в разделе реестра [AppID](appid-clsid.md) для сервера.</span><span class="sxs-lookup"><span data-stu-id="00e58-115">The DLL server surrogate runs in the same security context as the client, unless a **RunAs** value, which determines the security context, is set in the [AppID](appid-clsid.md) registry section for the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00e58-116">См. также</span><span class="sxs-lookup"><span data-stu-id="00e58-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00e58-117">Суррогаты библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="00e58-117">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




