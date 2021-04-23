---
title: Удаленный доступ к реестру в 64-разрядной версии Windows
description: Перенаправитель реестра обеспечивает удаленный доступ к реестру в 64-разрядной системе Windows с помощью функции Регконнектрегистри.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- удаленный доступ к реестру 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691514"
---
# <a name="remote-registry-access-in-64-bit-windows"></a><span data-ttu-id="17a4a-104">Удаленный доступ к реестру в 64-разрядной версии Windows</span><span class="sxs-lookup"><span data-stu-id="17a4a-104">Remote Registry Access in 64-bit Windows</span></span>

<span data-ttu-id="17a4a-105">Перенаправитель реестра обеспечивает удаленный доступ к реестру в 64-разрядной системе Windows с помощью функции [**регконнектрегистри**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .</span><span class="sxs-lookup"><span data-stu-id="17a4a-105">The registry redirector provides remote access to the registry on 64-bit Windows through the [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) function.</span></span>

<span data-ttu-id="17a4a-106">Если клиент является 32-битным приложением, он обращается к представлению реестра по умолчанию в 32-битном сервере.</span><span class="sxs-lookup"><span data-stu-id="17a4a-106">If the client is a 32-bit application, it accesses the server's default 32-bit registry view.</span></span> <span data-ttu-id="17a4a-107">Если клиент является 64-битным приложением, он обращается к представлению реестра с 64-битным реестром.</span><span class="sxs-lookup"><span data-stu-id="17a4a-107">If the client is a 64-bit application, it accesses the 64-bit registry view.</span></span>

<span data-ttu-id="17a4a-108">**Windows Server 2003:** Все клиенты получают доступ к 64-разрядному представлению реестра, если только приложение не использует \_ \_ флаг WOW64 32KEY.</span><span class="sxs-lookup"><span data-stu-id="17a4a-108">**Windows Server 2003:** All clients access the 64-bit registry view unless the application uses the KEY\_WOW64\_32KEY flag.</span></span> <span data-ttu-id="17a4a-109">Такое поведение изменилось при использовании Windows Server 2003 с пакетом обновления 1 (SP1) и Windows XP Professional x64 Edition при условии, что клиент и сервер работают под управлением этих версий Windows.</span><span class="sxs-lookup"><span data-stu-id="17a4a-109">This behavior changed with Windows Server 2003 with Service Pack 1 (SP1) and Windows XP Professional x64 Edition, provided that both the client and the server are running these versions of Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17a4a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="17a4a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17a4a-111">Перенаправитель реестра</span><span class="sxs-lookup"><span data-stu-id="17a4a-111">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="17a4a-112">Отражение реестра</span><span class="sxs-lookup"><span data-stu-id="17a4a-112">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 