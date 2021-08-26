---
title: Символ D3D12SDKVersion
description: Номер версии пакета SDK Direct3D 12.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/25/2021
req.lib: ''
req.dll: d3d12core.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d12core.dll
api_name:
- D3D12SDKVersion
targetos: Windows
ms.openlocfilehash: 0bf0aa17e16a4274b69e80580c0615ed055dd97a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917958"
---
# <a name="d3d12sdkversion-symbol"></a>Символ D3D12SDKVersion

Номер версии пакета SDK Direct3D 12.

## <a name="syntax"></a>Синтаксис

```cpp
extern "C" { _declspec(dllexport) extern const UINT D3D12SDKVersion = n;}
```

## <a name="return-value"></a>Возвращаемое значение

Значение типа [uint](/windows/win32/winprog/windows-data-types) , содержащее номер версии пакета SDK Direct3D 12.

## <a name="remarks"></a>Комментарии

**D3D12SDKVersion** не связан с библиотекой импорта или файлом заголовка.

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | Недоступно |
| **Библиотека** | Недоступно |
| **КОМПОНОВКИ** | d3d12core.dll |

## <a name="see-also"></a>См. также раздел
