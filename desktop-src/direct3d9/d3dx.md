---
description: D3DX — это библиотека средств, предназначенная для предоставления дополнительных графических функций на основе Direct3D. D3DX предоставляется в виде библиотеки динамической компоновки (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342212"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="bb1cf-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bb1cf-104">D3DX (Direct3D 9)</span></span>

<span data-ttu-id="bb1cf-105">D3DX — это библиотека средств, предназначенная для предоставления дополнительных графических функций на основе Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bb1cf-105">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="bb1cf-106">D3DX предоставляется в виде библиотеки динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="bb1cf-106">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="bb1cf-107">В этом выпуске пакета SDK для DirectX предоставляется только одна версия D3DX.</span><span class="sxs-lookup"><span data-stu-id="bb1cf-107">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="bb1cf-108">Библиотека Redistributable D3DX DLL включена в распространяемый пакет, предоставляемый в пакете SDK, и автоматически устанавливается в процессе [установки DirectX с помощью директсетуп](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="bb1cf-108">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span></span> <span data-ttu-id="bb1cf-109">Библиотека D3DX, включенная в этот выпуск, зависит от среды выполнения Direct3D, поставляемой с этим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="bb1cf-109">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="bb1cf-110">Приложения, связанные с версией D3DX в этом выпуске, также должны повторно распространять среду выполнения из этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="bb1cf-110">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="bb1cf-111">Несколько выпусков D3DX могут располагаться независимо на одной системе одновременно.</span><span class="sxs-lookup"><span data-stu-id="bb1cf-111">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="bb1cf-112">При статической компоновке приложения с D3dx9. lib приложение динамически связывается с соответствующей Retail D3DX DLL во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="bb1cf-112">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="bb1cf-113">Эта библиотека DLL соответствует заголовкам D3DX, для которых приложение компилируется в (с именем \_ с \_ константой версии пакета SDK D3DX в D3dx9core. h).</span><span class="sxs-lookup"><span data-stu-id="bb1cf-113">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="bb1cf-114">По мере выпуска новых версий D3DX в будущих выпусках пакета SDK для DirectX приложения, связанные с предыдущими библиотеками D3DX, останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="bb1cf-114">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="bb1cf-115">Библиотека D3DX устраняет следующие общие области функциональности:</span><span class="sxs-lookup"><span data-stu-id="bb1cf-115">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="bb1cf-116">Поддержка рисования линий в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bb1cf-116">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="bb1cf-117">Поддержка сеток в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bb1cf-117">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="bb1cf-118">Поддержка математических функций в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bb1cf-118">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="bb1cf-119">Поддержка текстур в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bb1cf-119">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="bb1cf-120">См. также</span><span class="sxs-lookup"><span data-stu-id="bb1cf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb1cf-121">Начало работы</span><span class="sxs-lookup"><span data-stu-id="bb1cf-121">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



