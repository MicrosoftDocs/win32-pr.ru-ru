---
description: В этом разделе содержатся сведения о функциях, предоставляемых DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: Функции DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536809"
---
# <a name="dxgi-functions"></a><span data-ttu-id="88f46-103">Функции DXGI</span><span class="sxs-lookup"><span data-stu-id="88f46-103">DXGI Functions</span></span>

<span data-ttu-id="88f46-104">В этом разделе содержатся сведения о функциях, предоставляемых DXGI.</span><span class="sxs-lookup"><span data-stu-id="88f46-104">This section contains info about the functions provided by DXGI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="88f46-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="88f46-105">In this section</span></span>



| <span data-ttu-id="88f46-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="88f46-106">Topic</span></span>                                                                                   | <span data-ttu-id="88f46-107">Описание</span><span class="sxs-lookup"><span data-stu-id="88f46-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88f46-108">**креатедксгифактори**</span><span class="sxs-lookup"><span data-stu-id="88f46-108">**CreateDXGIFactory**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | <span data-ttu-id="88f46-109">Создает фабрику DXGI 1,0, которую можно использовать для создания других объектов DXGI.</span><span class="sxs-lookup"><span data-stu-id="88f46-109">Creates a DXGI 1.0 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="88f46-110">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="88f46-110">**CreateDXGIFactory1**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | <span data-ttu-id="88f46-111">Создает фабрику DXGI 1,1, которую можно использовать для создания других объектов DXGI.</span><span class="sxs-lookup"><span data-stu-id="88f46-111">Creates a DXGI 1.1 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="88f46-112">**CreateDXGIFactory2**</span><span class="sxs-lookup"><span data-stu-id="88f46-112">**CreateDXGIFactory2**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | <span data-ttu-id="88f46-113">Создает фабрику DXGI 1,3, которую можно использовать для создания других объектов DXGI.</span><span class="sxs-lookup"><span data-stu-id="88f46-113">Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.</span></span><br/> <span data-ttu-id="88f46-114">В Windows 8 любая фабрика DXGI, созданная при наличии DXGIDebug.dll в системе, будет загружать и использовать ее.</span><span class="sxs-lookup"><span data-stu-id="88f46-114">In Windows 8, any DXGI factory created while DXGIDebug.dll was present on the system would load and use it.</span></span> <span data-ttu-id="88f46-115">Начиная с Windows 8.1, приложения явно запрашивают, что DXGIDebug.dll быть загружены.</span><span class="sxs-lookup"><span data-stu-id="88f46-115">Starting in Windows 8.1, apps explicitly request that DXGIDebug.dll be loaded instead.</span></span> <span data-ttu-id="88f46-116">Используйте [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) и укажите \_ \_ флаг создания отладочной фабрики DXGI \_ , чтобы запросить DXGIDebug.dll. Библиотека DLL будет загружена, если она есть в системе.</span><span class="sxs-lookup"><span data-stu-id="88f46-116">Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) and specify the DXGI\_CREATE\_FACTORY\_DEBUG flag to request DXGIDebug.dll; the DLL will be loaded if it is present on the system.</span></span><br/> |
| [<span data-ttu-id="88f46-117">**дксгидеклареадаптерремовалсуппорт**</span><span class="sxs-lookup"><span data-stu-id="88f46-117">**DXGIDeclareAdapterRemovalSupport**</span></span>](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | <span data-ttu-id="88f46-118">Позволяет процессу указать, что он устойчив к любому удаляемому графическому устройству.</span><span class="sxs-lookup"><span data-stu-id="88f46-118">Allows a process to indicate that it's resilient to any of its graphics devices being removed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="88f46-119">**дксгижетдебугинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="88f46-119">**DXGIGetDebugInterface**</span></span>](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | <span data-ttu-id="88f46-120">Извлекает интерфейс отладки.</span><span class="sxs-lookup"><span data-stu-id="88f46-120">Retrieves a debugging interface.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="88f46-121">**DXGIGetDebugInterface1**</span><span class="sxs-lookup"><span data-stu-id="88f46-121">**DXGIGetDebugInterface1**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | <span data-ttu-id="88f46-122">Извлекает интерфейс, используемый приложениями Магазина Windows для отладки графической инфраструктуры Microsoft DirectX (DXGI).</span><span class="sxs-lookup"><span data-stu-id="88f46-122">Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="88f46-123">См. также</span><span class="sxs-lookup"><span data-stu-id="88f46-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88f46-124">Ссылка на DXGI</span><span class="sxs-lookup"><span data-stu-id="88f46-124">DXGI Reference</span></span>](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




