---
title: Run-Time связывания с Wtsapi32.dll
description: Приложение может использовать службы удаленных рабочих столов API для динамической привязки к Wtsapi32.dll во время выполнения. Для этого приложение должно вызвать функцию LoadLibrary для загрузки Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413355"
---
# <a name="run-time-linking-to-wtsapi32dll"></a><span data-ttu-id="a5dfe-104">Run-Time связывания с Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="a5dfe-104">Run-Time linking to Wtsapi32.dll</span></span>

<span data-ttu-id="a5dfe-105">Если приложение работает в среде, которая не является средой службы удаленных рабочих столов, но требуется, чтобы приложение предоставляющо дополнительные функциональные возможности при запуске в среде службы удаленных рабочих столов, приложение может использовать API службы удаленных рабочих столов для реализации дополнительных функций и динамически связываться с Wtsapi32.dll во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a5dfe-105">If your application runs in an environment that is not a Remote Desktop Services environment, but you want your application to provide additional functionality when it does run in a Remote Desktop Services environment, the application can use the Remote Desktop Services API to implement the additional functionality, and dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="a5dfe-106">Для этого приложение должно вызвать функцию [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) для загрузки Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a5dfe-106">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span> <span data-ttu-id="a5dfe-107">В случае сбоя вызова **LoadLibrary** приложение может выполняться с использованием базовых функций.</span><span class="sxs-lookup"><span data-stu-id="a5dfe-107">If the **LoadLibrary** call fails, your application can run using its basic functionality.</span></span> <span data-ttu-id="a5dfe-108">Если **LoadLibrary** выполняется, приложение может вызвать функцию [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения указателей на службы удаленных рабочих столов функции, которые необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="a5dfe-108">If **LoadLibrary** succeeds, your application can call the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve pointers to the Remote Desktop Services functions that you want to call.</span></span>

<span data-ttu-id="a5dfe-109">Если приложение предназначено только для среды службы удаленных рабочих столов, динамическая компоновка не требуется.</span><span class="sxs-lookup"><span data-stu-id="a5dfe-109">If your application is intended only for a Remote Desktop Services environment, dynamic linking is not necessary.</span></span> <span data-ttu-id="a5dfe-110">В этом случае можно включить Wtsapi32. h и связать с Wtsapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="a5dfe-110">In this case, you can include Wtsapi32.h and link with Wtsapi32.lib.</span></span> <span data-ttu-id="a5dfe-111">Затем, если приложение запускается в среде, отличной от службы удаленных рабочих столов, она будет закрыта, так как отсутствует Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a5dfe-111">Then, if your application starts up in an environment other than Remote Desktop Services, it will exit because Wtsapi32.dll is not present.</span></span>

<span data-ttu-id="a5dfe-112">Сведения о том, как определить, выполняется ли приложение в среде службы удаленных рабочих столов, см. в разделе [Обнаружение среды службы удаленных рабочих столов](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a5dfe-112">For information about determining whether your application is running in a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5dfe-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a5dfe-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5dfe-114">Общие рекомендации по программированию</span><span class="sxs-lookup"><span data-stu-id="a5dfe-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> </dl>

 

 