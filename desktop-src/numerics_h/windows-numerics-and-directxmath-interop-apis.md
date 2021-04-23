---
title: Числовые API-интерфейсы Windows и Директксмас Interop (Виндовснумерикс. h)
description: Эти функции преобразуют типы Windows. Foundation. numeric в и из Директксмас SIMD Types КСМВЕКТОР и КСММАТРИКС.
ms.assetid: 05851054-196E-4955-B9C5-85C2E33EF488
keywords:
- Функции numeric и Директксмас Interop API
topic_type:
- apiref
api_name:
- WWindows numerics and DirectXMath interop APIs
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e39057c92eeed87c3f429acb56f0afa2468ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721041"
---
# <a name="windows-numerics-and-directxmath-interop-apis"></a><span data-ttu-id="fbfb5-104">Функции numeric и Директксмас Interop API</span><span class="sxs-lookup"><span data-stu-id="fbfb5-104">Windows numerics and DirectXMath interop APIs</span></span>

<span data-ttu-id="fbfb5-105">Эти функции преобразуют типы [**Windows. Foundation. numeric**](/uwp/api/Windows.Foundation.Numerics) в и из директксмас SIMD Types [ксмвектор](../dxmath/xmvector-data-type.md) и [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="fbfb5-105">These functions convert [**Windows.Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) types to and from the DirectXMath SIMD types [XMVECTOR](../dxmath/xmvector-data-type.md) and [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span>

## <a name="functions"></a><span data-ttu-id="fbfb5-106">Функции</span><span class="sxs-lookup"><span data-stu-id="fbfb5-106">Functions</span></span>

| <span data-ttu-id="fbfb5-107">Имя</span><span class="sxs-lookup"><span data-stu-id="fbfb5-107">Name</span></span> | <span data-ttu-id="fbfb5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fbfb5-108">Description</span></span> |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | <span data-ttu-id="fbfb5-109">Загружает float2 в Директксмас [ксмвектор](../dxmath/xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="fbfb5-109">Loads a float2 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | <span data-ttu-id="fbfb5-110">Загружает float3 в Директксмас [ксмвектор](../dxmath/xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="fbfb5-110">Loads a float3 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | <span data-ttu-id="fbfb5-111">Загружает float4 в Директксмас [ксмвектор](../dxmath/xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="fbfb5-111">Loads a float4 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | <span data-ttu-id="fbfb5-112">Загружает float3x2 в Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="fbfb5-112">Loads a float3x2 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | <span data-ttu-id="fbfb5-113">Загружает float4x4 в Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="fbfb5-113">Loads a float4x4 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | <span data-ttu-id="fbfb5-114">Загружает плоскость в [Ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)директксмас.</span><span class="sxs-lookup"><span data-stu-id="fbfb5-114">Loads a plane into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | <span data-ttu-id="fbfb5-115">Загружает кватернион в Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="fbfb5-115">Loads a quaternion into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="fbfb5-116">Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в float2.</span><span class="sxs-lookup"><span data-stu-id="fbfb5-116">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float2.</span></span> |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="fbfb5-117">Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в float3.</span><span class="sxs-lookup"><span data-stu-id="fbfb5-117">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float3.</span></span> |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="fbfb5-118">Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в float4.</span><span class="sxs-lookup"><span data-stu-id="fbfb5-118">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float4.</span></span> |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="fbfb5-119">Сохраняет Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) в float3x2.</span><span class="sxs-lookup"><span data-stu-id="fbfb5-119">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float3x2.</span></span> |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="fbfb5-120">Сохраняет Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) в float4x4.</span><span class="sxs-lookup"><span data-stu-id="fbfb5-120">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float4x4.</span></span> |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="fbfb5-121">Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в плоскости.</span><span class="sxs-lookup"><span data-stu-id="fbfb5-121">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a plane.</span></span> |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="fbfb5-122">Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в кватернион.</span><span class="sxs-lookup"><span data-stu-id="fbfb5-122">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="fbfb5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fbfb5-123">Requirements</span></span>

| <span data-ttu-id="fbfb5-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fbfb5-124">Requirement</span></span> | <span data-ttu-id="fbfb5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfb5-125">Value</span></span> |
|-|-|
| <span data-ttu-id="fbfb5-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fbfb5-126">Namespace</span></span> | <span data-ttu-id="fbfb5-127">DirectX</span><span class="sxs-lookup"><span data-stu-id="fbfb5-127">DirectX</span></span> |
| <span data-ttu-id="fbfb5-128">Header</span><span class="sxs-lookup"><span data-stu-id="fbfb5-128">Header</span></span> | <dl> <span data-ttu-id="fbfb5-129"><dt>Виндовснумерикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbfb5-129"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="fbfb5-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbfb5-130">See also</span></span>

[<span data-ttu-id="fbfb5-131">API-интерфейсы виндовснумерикс. h</span><span class="sxs-lookup"><span data-stu-id="fbfb5-131">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
