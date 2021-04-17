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
# <a name="windows-numerics-and-directxmath-interop-apis"></a>Функции numeric и Директксмас Interop API

Эти функции преобразуют типы [**Windows. Foundation. numeric**](/uwp/api/Windows.Foundation.Numerics) в и из директксмас SIMD Types [ксмвектор](../dxmath/xmvector-data-type.md) и [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).

## <a name="functions"></a>Функции

| Имя | Описание |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | Загружает float2 в Директксмас [ксмвектор](../dxmath/xmvector-data-type.md). |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | Загружает float3 в Директксмас [ксмвектор](../dxmath/xmvector-data-type.md). |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | Загружает float4 в Директксмас [ксмвектор](../dxmath/xmvector-data-type.md). |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | Загружает float3x2 в Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | Загружает float4x4 в Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | Загружает плоскость в [Ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)директксмас. |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | Загружает кватернион в Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в float2. |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в float3. |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в float4. |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | Сохраняет Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) в float3x2. |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | Сохраняет Директксмас [ксмматрикс](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) в float4x4. |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в плоскости. |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | Сохраняет Директксмас [ксмвектор](../dxmath/xmvector-data-type.md) в кватернион. |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Пространство имен | DirectX |
| Header | <dl> <dt>Виндовснумерикс. h</dt> </dl> |

## <a name="see-also"></a>См. также раздел

[API-интерфейсы виндовснумерикс. h](windowsnumerics-h-apis-portal.md)
