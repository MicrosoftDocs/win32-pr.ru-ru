---
title: Общие интерфейсы версий
description: В этом разделе содержатся сведения об интерфейсах общих версий.
ms.assetid: d228c3c2-e2ff-4723-aec1-5c3ce82c321d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f535650fa24593cc4b663c1a2b01a1a2d53a9b3b
ms.sourcegitcommit: 8f833c83be1accc119cc57e67b608ffe1e0159b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/07/2020
ms.locfileid: "103797161"
---
# <a name="common-version-interfaces"></a><span data-ttu-id="9f70d-103">Общие интерфейсы версий</span><span class="sxs-lookup"><span data-stu-id="9f70d-103">Common version interfaces</span></span>

<span data-ttu-id="9f70d-104">В этом разделе содержатся сведения об интерфейсах общих версий.</span><span class="sxs-lookup"><span data-stu-id="9f70d-104">This section contains information about the common version interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9f70d-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9f70d-105">In this section</span></span>

| <span data-ttu-id="9f70d-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="9f70d-106">Topic</span></span> | <span data-ttu-id="9f70d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9f70d-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="9f70d-108">**ID3D10Blob**</span><span class="sxs-lookup"><span data-stu-id="9f70d-108">**ID3D10Blob**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3d10blob) | <span data-ttu-id="9f70d-109">Этот интерфейс используется для возврата данных произвольной длины.</span><span class="sxs-lookup"><span data-stu-id="9f70d-109">This interface is used to return arbitrary-length data.</span></span> |
| <span data-ttu-id="9f70d-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9f70d-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span> | <span data-ttu-id="9f70d-111">Этот интерфейс используется для возврата данных произвольной длины.</span><span class="sxs-lookup"><span data-stu-id="9f70d-111">This interface is used to return data of arbitrary length.</span></span> |
| [<span data-ttu-id="9f70d-112">**ID3DDestructionNotifier**</span><span class="sxs-lookup"><span data-stu-id="9f70d-112">**ID3DDestructionNotifier**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier) | <span data-ttu-id="9f70d-113">Используется для регистрации обратных вызовов при удалении прямого трехмерного объекта Nano-COM.</span><span class="sxs-lookup"><span data-stu-id="9f70d-113">Used to register for callbacks when a Direct 3D nano-COM object is destroyed.</span></span> |
| [<span data-ttu-id="9f70d-114">**ID3DInclude**</span><span class="sxs-lookup"><span data-stu-id="9f70d-114">**ID3DInclude**</span></span>](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) | <span data-ttu-id="9f70d-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) — это интерфейс включения, который пользователь реализует, чтобы позволить приложению вызывать методы, переопределяемые пользователем, для открытия и закрытия \# файлов включения шейдера.</span><span class="sxs-lookup"><span data-stu-id="9f70d-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader \#include files.</span></span> |
| [<span data-ttu-id="9f70d-116">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="9f70d-116">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) | <span data-ttu-id="9f70d-117">Интерфейс [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) позволяет приложению описывать концептуальные разделы и маркеры в потоке кода приложения.</span><span class="sxs-lookup"><span data-stu-id="9f70d-117">The [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) interface enables an application to describe conceptual sections and markers within the application's code flow.</span></span> <span data-ttu-id="9f70d-118">Средство с соответствующим параметром, например Microsoft Visual Studio Ultimate 2012, может отображать эти разделы и маркеры визуально на строке времени Microsoft Direct3D средства, а средство выдает ошибку в приложении.</span><span class="sxs-lookup"><span data-stu-id="9f70d-118">An appropriately enabled tool, such as Microsoft Visual Studio Ultimate 2012, can display these sections and markers visually along the tool's Microsoft Direct3D time line, while the tool debugs the application.</span></span> <span data-ttu-id="9f70d-119">Эти визуальные заметки позволяют пользователям такого инструмента переходить к частям интересующей строки времени или понимать, какой набор вызовов Direct3D создается определенными частями кода приложения.</span><span class="sxs-lookup"><span data-stu-id="9f70d-119">These visual notes allow users of such a tool to navigate to parts of the time line that are of interest, or to understand what set of Direct3D calls are produced by certain sections of the application's code.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="9f70d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="9f70d-120">Related topics</span></span>

[<span data-ttu-id="9f70d-121">Ссылка на стандартную версию</span><span class="sxs-lookup"><span data-stu-id="9f70d-121">Common version reference</span></span>](d3d11-graphics-reference-d3d11-common.md)
