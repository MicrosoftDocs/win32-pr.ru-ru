---
description: 'Запрос на запуск отладки шейдера. Этот запрос состоит из двух частей: создание трассировки и отладка трассировки.'
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IDebugShaderRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7b7c183cc04422d47b8d6599c67f2e7c1f5e58cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140067"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span data-ttu-id="8e94b-104"><span id="vspixengine.idebugshaderrequest2"></span>Интерфейс IDebugShaderRequest2</span><span class="sxs-lookup"><span data-stu-id="8e94b-104"><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2 interface</span></span>

<span data-ttu-id="8e94b-105">Запрос на запуск отладки шейдера.</span><span class="sxs-lookup"><span data-stu-id="8e94b-105">Request to start debugging a shader.</span></span> <span data-ttu-id="8e94b-106">Этот запрос состоит из двух частей: создание трассировки и отладка трассировки.</span><span class="sxs-lookup"><span data-stu-id="8e94b-106">This request contains two parts: generate a trace, and debug a trace.</span></span>

## <a name="members"></a><span data-ttu-id="8e94b-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="8e94b-107">Members</span></span>

<span data-ttu-id="8e94b-108">Интерфейс **IDebugShaderRequest2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8e94b-108">The **IDebugShaderRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8e94b-109">**IDebugShaderRequest2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8e94b-109">**IDebugShaderRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="8e94b-110">Методы</span><span class="sxs-lookup"><span data-stu-id="8e94b-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="8e94b-111"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="8e94b-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="8e94b-112">Интерфейс **IDebugShaderRequest2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8e94b-112">The **IDebugShaderRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="8e94b-113">Метод</span><span class="sxs-lookup"><span data-stu-id="8e94b-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="8e94b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8e94b-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="8e94b-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>бегиндебугшадер</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e94b-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8e94b-116">Запросы на запуск отладки указанного списка инструкций.</span><span class="sxs-lookup"><span data-stu-id="8e94b-116">Requests to start debugging the specified list of instructions.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="8e94b-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>женератеинструктионс</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e94b-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8e94b-118">Запросы на создание инструкций трассировки шейдера в отладочном запросе.</span><span class="sxs-lookup"><span data-stu-id="8e94b-118">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="8e94b-119">Отладка на основе трассировки происходит в ЦП (деформацию), а не на GPU.</span><span class="sxs-lookup"><span data-stu-id="8e94b-119">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="8e94b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8e94b-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8e94b-121">Header</span><span class="sxs-lookup"><span data-stu-id="8e94b-121">Header</span></span></p></td><td><span data-ttu-id="8e94b-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="8e94b-122">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
