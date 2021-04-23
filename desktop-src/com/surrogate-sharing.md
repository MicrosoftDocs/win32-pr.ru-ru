---
title: Общий доступ к суррогатам
description: Серверы DLL будут совместно использовать суррогат, если они совпадают с удостоверениями безопасности и имеют одинаковое значение AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774960"
---
# <a name="surrogate-sharing"></a><span data-ttu-id="f313d-103">Общий доступ к суррогатам</span><span class="sxs-lookup"><span data-stu-id="f313d-103">Surrogate Sharing</span></span>

<span data-ttu-id="f313d-104">Серверы DLL будут совместно использовать суррогат, если они совпадают с удостоверениями безопасности и имеют одинаковое значение AppID.</span><span class="sxs-lookup"><span data-stu-id="f313d-104">DLL servers will share a surrogate if they have matching security identities and share the same AppID value.</span></span>

<span data-ttu-id="f313d-105">По умолчанию серверы DLL загружаются в собственный суррогатный процесс.</span><span class="sxs-lookup"><span data-stu-id="f313d-105">DLL servers are loaded, by default, into their own surrogate process.</span></span> <span data-ttu-id="f313d-106">Чтобы загрузить другие серверы DLL в существующий суррогат, чтобы он поддерживал более одного сервера DLL, необходимо выполнить два требования.</span><span class="sxs-lookup"><span data-stu-id="f313d-106">To load other DLL servers into an existing surrogate so that it supports more than one DLL server, there are two requirements:</span></span>

-   <span data-ttu-id="f313d-107">Серверы DLL должны иметь одинаковое значение AppID.</span><span class="sxs-lookup"><span data-stu-id="f313d-107">The DLL servers must have the same AppID value.</span></span>
-   <span data-ttu-id="f313d-108">Контекст безопасности серверов DLL должен быть одним и тем же.</span><span class="sxs-lookup"><span data-stu-id="f313d-108">The security context of the DLL servers must be the same.</span></span>

<span data-ttu-id="f313d-109">Если два сервера DLL должны запускаться с разными идентификаторами безопасности, они должны находиться в разных суррогатах, независимо от того, совпадают ли их идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="f313d-109">If two DLL servers are to be launched under different security identities, they must be in different surrogates, whether their AppIDs match.</span></span>

<span data-ttu-id="f313d-110">Ниже приведен пример администрирования общего доступа к суррогатам с AppID.</span><span class="sxs-lookup"><span data-stu-id="f313d-110">Following is an example of administering surrogate sharing with AppIDs:</span></span>

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

<span data-ttu-id="f313d-111">Два идентификатора CLSID для компонентов DLL comp1.dll и comp2.dll настроены для совместного использования AppID.</span><span class="sxs-lookup"><span data-stu-id="f313d-111">The two CLSIDs for DLL components comp1.dll and comp2.dll have been configured to share an AppID.</span></span> <span data-ttu-id="f313d-112">Ключ [AppID](appid-key.md) указывает, что сервер DLL можно загрузить в суррогат, указав значение [дллсуррогате](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="f313d-112">The [AppID](appid-key.md) key specifies that the DLL server can be loaded in a surrogate by specifying the [DllSurrogate](dllsurrogate.md) value.</span></span> <span data-ttu-id="f313d-113">В этом примере значение **дллсуррогате** — это пустая строка, указывающая, что следует использовать системную реализацию СУРРОГАТНОЙ библиотеки DLL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f313d-113">In this example, the **DllSurrogate** value is an empty string, indicating that the default system implementation of the DLL surrogate should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f313d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f313d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f313d-115">Требования к серверу DLL</span><span class="sxs-lookup"><span data-stu-id="f313d-115">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="f313d-116">Регистрация сервера DLL для активации суррогатных символов</span><span class="sxs-lookup"><span data-stu-id="f313d-116">Registering the DLL Server for Surrogate Activation</span></span>](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




