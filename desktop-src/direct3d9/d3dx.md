---
description: D3DX — это библиотека средств, предназначенная для предоставления дополнительных графических функций на основе Direct3D. D3DX предоставляется в виде библиотеки динамической компоновки (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a2164349b761cd7ff2ccca5e2158abc22bd64
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910252"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="61c9f-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="61c9f-104">D3DX (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="61c9f-105">Библиотека D3DX устарела.</span><span class="sxs-lookup"><span data-stu-id="61c9f-105">The D3DX library is deprecated.</span></span> <span data-ttu-id="61c9f-106">Если обновление до более новой версии Direct3D и связанного с ней кода не является допустимым вариантом, можно использовать пакет NuGet [Microsoft. дкссдк. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) вместо использования УСТАРЕВШЕГО пакета SDK DirectX или директсетуп.</span><span class="sxs-lookup"><span data-stu-id="61c9f-106">If upgrading to a newer version of Direct3D and associated utility code is not an option, you can make use of the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package rather than relying on the legacy DirectX SDK or DirectSetup.</span></span>

<span data-ttu-id="61c9f-107">D3DX — это библиотека средств, предназначенная для предоставления дополнительных графических функций на основе Direct3D.</span><span class="sxs-lookup"><span data-stu-id="61c9f-107">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="61c9f-108">D3DX предоставляется в виде библиотеки динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="61c9f-108">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="61c9f-109">В этом выпуске пакета SDK для DirectX предоставляется только одна версия D3DX.</span><span class="sxs-lookup"><span data-stu-id="61c9f-109">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="61c9f-110">Библиотека Redistributable D3DX DLL включена в распространяемый пакет, предоставляемый в пакете SDK, и автоматически устанавливается в процессе **установки DirectX с помощью директсетуп**.</span><span class="sxs-lookup"><span data-stu-id="61c9f-110">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of **Installing DirectX with DirectSetup**.</span></span> <span data-ttu-id="61c9f-111">Библиотека D3DX, включенная в этот выпуск, зависит от среды выполнения Direct3D, поставляемой с этим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="61c9f-111">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="61c9f-112">Приложения, связанные с версией D3DX в этом выпуске, также должны повторно распространять среду выполнения из этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="61c9f-112">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="61c9f-113">Несколько выпусков D3DX могут располагаться независимо на одной системе одновременно.</span><span class="sxs-lookup"><span data-stu-id="61c9f-113">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="61c9f-114">При статической компоновке приложения с D3dx9. lib приложение динамически связывается с соответствующей Retail D3DX DLL во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="61c9f-114">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="61c9f-115">Эта библиотека DLL соответствует заголовкам D3DX, для которых приложение компилируется в (с именем \_ с \_ константой версии пакета SDK D3DX в D3dx9core. h).</span><span class="sxs-lookup"><span data-stu-id="61c9f-115">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="61c9f-116">По мере выпуска новых версий D3DX в будущих выпусках пакета SDK для DirectX приложения, связанные с предыдущими библиотеками D3DX, останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="61c9f-116">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="61c9f-117">Библиотека D3DX устраняет следующие общие области функциональности:</span><span class="sxs-lookup"><span data-stu-id="61c9f-117">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="61c9f-118">Поддержка рисования линий в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="61c9f-118">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="61c9f-119">Поддержка сеток в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="61c9f-119">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="61c9f-120">Поддержка математических функций в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="61c9f-120">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="61c9f-121">Поддержка текстур в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="61c9f-121">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="61c9f-122">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="61c9f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61c9f-123">Начало работы</span><span class="sxs-lookup"><span data-stu-id="61c9f-123">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



