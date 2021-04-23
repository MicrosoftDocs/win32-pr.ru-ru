---
title: Работа с Direct3D 11, Direct3D 10 и Direct2D
description: В этом разделе рассматриваются методы взаимодействия с более ранними версиями Direct3D и Direct2D, API-интерфейсом Direct3D 11on12 и правилами переноса с Direct3D 11 на Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103506"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a><span data-ttu-id="402e2-103">Работа с Direct3D 11, Direct3D 10 и Direct2D</span><span class="sxs-lookup"><span data-stu-id="402e2-103">Working with Direct3D 11, Direct3D 10 and Direct2D</span></span>

<span data-ttu-id="402e2-104">В этом разделе рассматриваются методы взаимодействия с более ранними версиями Direct3D и Direct2D, API-интерфейсом Direct3D 11on12 и правилами переноса с Direct3D 11 на Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="402e2-104">This section covers interop techniques with earlier versions of Direct3D and Direct2D, the Direct3D 11on12 API, and porting guidelines from Direct3D 11 to Direct3D 12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="402e2-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="402e2-105">In this section</span></span>



| <span data-ttu-id="402e2-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="402e2-106">Topic</span></span>                                                                                             | <span data-ttu-id="402e2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="402e2-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="402e2-108">Взаимодействие Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="402e2-108">Direct3D 12 Interop</span></span>](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | <span data-ttu-id="402e2-109">D3D12 можно использовать для написания компонентных приложений.</span><span class="sxs-lookup"><span data-stu-id="402e2-109">D3D12 can be used to write componentized applications.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="402e2-110">Direct3D 11 на 12</span><span class="sxs-lookup"><span data-stu-id="402e2-110">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)<br/>                                             | <span data-ttu-id="402e2-111">D3D11On12 — это механизм, с помощью которого разработчики могут использовать интерфейсы и объекты D3D11 для управления API D3D12.</span><span class="sxs-lookup"><span data-stu-id="402e2-111">D3D11On12 is a mechanism by which developers can use D3D11 interfaces and objects to drive the D3D12 API.</span></span> <span data-ttu-id="402e2-112">D3D11on12 позволяет компонентам, написанным с помощью D3D11 (например, к тексту и пользовательскому интерфейсу D2D), работать вместе с компонентами, предназначенными для API D3D12.</span><span class="sxs-lookup"><span data-stu-id="402e2-112">D3D11on12 enables components written using D3D11 (for example, D2D text and UI) to work together with components written targeting the D3D12 API.</span></span> <span data-ttu-id="402e2-113">D3D11on12 также позволяет выполнять добавочное перенос приложения из D3D11 в D3D12, позволяя частям приложения продолжить нацеливание на D3D11 для простоты, в то время как другие нацелены на D3D12 для повышения производительности, в то же время всегда Завершая и исправлять отрисовку.</span><span class="sxs-lookup"><span data-stu-id="402e2-113">D3D11on12 also enables incremental porting of an application from D3D11 to D3D12, by enabling portions of the app to continue targeting D3D11 for simplicity while others target D3D12 for performance, while always having complete and correct rendering.</span></span> <span data-ttu-id="402e2-114">D3D11On12 делает его проще, чем использование методов взаимодействия для совместного использования ресурсов и синхронизации работы между двумя API.</span><span class="sxs-lookup"><span data-stu-id="402e2-114">D3D11On12 makes it simpler than using interop techniques to share resources and synchronize work between the two APIs.</span></span> <br/> |
| [<span data-ttu-id="402e2-115">Перенос из Direct3D 11 в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="402e2-115">Porting from Direct3D 11 to Direct3D 12</span></span>](porting-from-direct3d-11-to-direct3d-12.md)<br/> | <span data-ttu-id="402e2-116">В этом разделе приводятся некоторые рекомендации по переносу из пользовательского графического подсистемы Direct3D 11 в Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="402e2-116">This section provides some guidance on porting from a custom Direct3D 11 graphics engine to Direct3D 12.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="402e2-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="402e2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="402e2-118">Руководство по программированию для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="402e2-118">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





