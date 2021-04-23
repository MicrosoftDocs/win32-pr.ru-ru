---
title: Взаимодействие
description: Описывает, как Direct2D взаимодействует с другими системами.
ms.assetid: 538e0ff7-50a8-40e2-ab34-d3eb6b7d0c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 872a090980618548fd73e43c6f82644962b8bd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134038"
---
# <a name="interoperability"></a><span data-ttu-id="af4c9-103">Совместимость</span><span class="sxs-lookup"><span data-stu-id="af4c9-103">Interoperability</span></span>

<span data-ttu-id="af4c9-104">В подразделах этого раздела описывается, как Direct2D взаимодействует с другими системами, такими как GDI, Direct3D и WIC.</span><span class="sxs-lookup"><span data-stu-id="af4c9-104">The topics in this section describe how Direct2D interoperates with other systems, such as GDI, Direct3D, and WIC.</span></span>

> [!Note]  
> <span data-ttu-id="af4c9-105">Начиная с Windows 8, Direct2D предоставляет интерфейс [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) , который обеспечивает простой способ взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="af4c9-105">Starting with Windows 8, Direct2D provides the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface which provides a simple way to interoperate.</span></span> <span data-ttu-id="af4c9-106">Дополнительные сведения см. в разделе [устройства и контексты устройств](devices-and-device-contexts.md) .</span><span class="sxs-lookup"><span data-stu-id="af4c9-106">See the [Devices and Device Contexts](devices-and-device-contexts.md) topic for more info.</span></span>

 



| <span data-ttu-id="af4c9-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="af4c9-107">Topic</span></span>                                                                                                           | <span data-ttu-id="af4c9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="af4c9-108">Description</span></span>                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af4c9-109">Общие сведения о взаимодействии</span><span class="sxs-lookup"><span data-stu-id="af4c9-109">Interoperability Overview</span></span>](interoperability-overview.md)<br/>                                           | <span data-ttu-id="af4c9-110">Содержит сводку по различным технологиям, которые можно использовать с Direct2D.</span><span class="sxs-lookup"><span data-stu-id="af4c9-110">Summarizes the different technologies you can use with Direct2D.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="af4c9-111">Общие сведения о взаимодействии Direct2D и GDI</span><span class="sxs-lookup"><span data-stu-id="af4c9-111">Direct2D and GDI Interoperability Overview</span></span>](direct2d-and-gdi-interoperation-overview.md)<br/>           | <span data-ttu-id="af4c9-112">Описывает, как использовать Direct2D и GDI совместно.</span><span class="sxs-lookup"><span data-stu-id="af4c9-112">Describes how to use Direct2D and GDI together.</span></span><br/>                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="af4c9-113">Сравнение аппаратного ускорения Direct2D и GDI</span><span class="sxs-lookup"><span data-stu-id="af4c9-113">Comparing Direct2D and GDI Hardware Acceleration</span></span>](comparing-direct2d-and-gdi.md)<br/>                   | <span data-ttu-id="af4c9-114">[Direct2D](./direct2d-portal.md) и [GDI](/windows/desktop/gdi/windows-gdi) являются API-интерфейсами двухмерной отрисовки в режиме интерпретации и имеют некоторую степень аппаратного ускорения.</span><span class="sxs-lookup"><span data-stu-id="af4c9-114">[Direct2D](./direct2d-portal.md) and [GDI](/windows/desktop/gdi/windows-gdi) are both immediate mode 2D rendering APIs and both offer some degree of hardware acceleration.</span></span> <span data-ttu-id="af4c9-115">В этом разделе рассматриваются различия между Direct2D и GDI, включая предыдущие и представляющие различия в функциях аппаратного ускорения обоих API.</span><span class="sxs-lookup"><span data-stu-id="af4c9-115">This topic explores the differences between Direct2D and GDI, including past and present differences in the hardware acceleration features of both APIs.</span></span><br/> |
| [<span data-ttu-id="af4c9-116">Общие сведения о взаимодействии Direct2D и Direct3D</span><span class="sxs-lookup"><span data-stu-id="af4c9-116">Direct2D and Direct3D Interoperability Overview</span></span>](direct2d-and-direct3d-interoperation-overview.md)<br/> | <span data-ttu-id="af4c9-117">Описывает, как использовать Direct2D и Direct3D 10 вместе.</span><span class="sxs-lookup"><span data-stu-id="af4c9-117">Describes how to use Direct2D and Direct3D 10 together.</span></span><br/>                                                                                                                                                                                                                                                                     |



 

 

