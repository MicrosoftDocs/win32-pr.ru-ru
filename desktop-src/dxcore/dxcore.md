---
title: DXCore
description: Дкскоре — это API перечисления адаптеров для устройств DirectX.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: 80e93ac7440629a809cb01b4d1d4fa2e73b7ee91
ms.sourcegitcommit: aa021b23d7e8bba2e1df9de93a1c315a17681810
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "105719180"
---
# <a name="dxcore"></a><span data-ttu-id="8cf8a-103">DXCore</span><span class="sxs-lookup"><span data-stu-id="8cf8a-103">DXCore</span></span>

<span data-ttu-id="8cf8a-104">Дкскоре — это API перечисления адаптеров для графических и расчетных устройств, поэтому некоторые его средства перекрываются с функциями [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="8cf8a-104">DXCore is an adapter enumeration API for graphics and compute devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span> <span data-ttu-id="8cf8a-105">Дкскоре используется Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="8cf8a-105">DXCore is used by Direct3D 12.</span></span>

<span data-ttu-id="8cf8a-106">Этот набор документации содержит сведения о программировании с помощью Дкскоре, а также справочник по Дкскоре.</span><span class="sxs-lookup"><span data-stu-id="8cf8a-106">This documentation set contains information about programming with DXCore, as well as the DXCore reference.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf8a-107">Требования</span><span class="sxs-lookup"><span data-stu-id="8cf8a-107">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8cf8a-108">**Поддерживаемые среды выполнения**</span><span class="sxs-lookup"><span data-stu-id="8cf8a-108">**Supported runtime environments**</span></span> | <span data-ttu-id="8cf8a-109">Windows/C++</span><span class="sxs-lookup"><span data-stu-id="8cf8a-109">Windows/C++</span></span> |
| <span data-ttu-id="8cf8a-110">**Рекомендуемые языки программирования**</span><span class="sxs-lookup"><span data-stu-id="8cf8a-110">**Recommended programming languages**</span></span> | <span data-ttu-id="8cf8a-111">C++</span><span class="sxs-lookup"><span data-stu-id="8cf8a-111">C++</span></span> |
| <span data-ttu-id="8cf8a-112">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="8cf8a-112">**Minimum supported client**</span></span> | <span data-ttu-id="8cf8a-113">Windows 10, версия 2004 (10,0; Сборка 19041)</span><span class="sxs-lookup"><span data-stu-id="8cf8a-113">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="8cf8a-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="8cf8a-114">**Header**</span></span> | <span data-ttu-id="8cf8a-115">дкскоре. h и dxcore_interface. h</span><span class="sxs-lookup"><span data-stu-id="8cf8a-115">dxcore.h and dxcore_interface.h</span></span> |
| <span data-ttu-id="8cf8a-116">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="8cf8a-116">**Library**</span></span> | <span data-ttu-id="8cf8a-117">дкскоре. lib</span><span class="sxs-lookup"><span data-stu-id="8cf8a-117">dxcore.lib</span></span> |
| <span data-ttu-id="8cf8a-118">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="8cf8a-118">**DLL**</span></span> | <span data-ttu-id="8cf8a-119">dxcore.dll</span><span class="sxs-lookup"><span data-stu-id="8cf8a-119">dxcore.dll</span></span> |

## <a name="in-this-section"></a><span data-ttu-id="8cf8a-120">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="8cf8a-120">In this section</span></span>

| <span data-ttu-id="8cf8a-121">Раздел</span><span class="sxs-lookup"><span data-stu-id="8cf8a-121">Topic</span></span> | <span data-ttu-id="8cf8a-122">Описание</span><span class="sxs-lookup"><span data-stu-id="8cf8a-122">Description</span></span> |
|-|-|
| [<span data-ttu-id="8cf8a-123">Руководство по программированию для DXCore</span><span class="sxs-lookup"><span data-stu-id="8cf8a-123">DXCore programming guide</span></span>](dxcore-programming-guide.md) | <span data-ttu-id="8cf8a-124">Руководство по программированию с помощью Дкскоре.</span><span class="sxs-lookup"><span data-stu-id="8cf8a-124">Guidance for programming with DXCore.</span></span> |
| [<span data-ttu-id="8cf8a-125">Справочные материалы по DXCore</span><span class="sxs-lookup"><span data-stu-id="8cf8a-125">DXCore reference</span></span>](dxcore-reference.md) | <span data-ttu-id="8cf8a-126">В этом разделе рассматриваются API-интерфейсы Дкскоре, объявленные в дкскоре. h и dxcore_interface. h.</span><span class="sxs-lookup"><span data-stu-id="8cf8a-126">This section covers DXCore APIs declared in dxcore.h and dxcore_interface.h.</span></span> |
