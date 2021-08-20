---
title: Функция D3D12IsLayoutOpaque (D3dx12. h)
description: Указывает, является ли макет непрозрачным.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- Функция D3D12IsLayoutOpaque
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db512ac96e4df41f3fc70d15cd8286a191cd56dd5e862d4061df4d69cd10ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098137"
---
# <a name="d3d12islayoutopaque-function"></a>Функция D3D12IsLayoutOpaque

Указывает, является ли макет непрозрачным.

## <a name="syntax"></a>Синтаксис


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Макет* 
</dt> <dd>

Тип: **[ **\_ \_ Макет текстуры D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**

Макет, который необходимо проверить, в [**виде \_ \_ макета текстуры D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **bool** .

**Логическое** значение, указывающее, является ли макет непрозрачным. Макет является непрозрачным, если он \_ имеет \_ вид текстуры D3D12 \_ НЕизвестный или D3D12ный \_ \_ Макет текстуры \_ 64 КБ \_ неопределенный \_ свиззле.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вспомогательные функции для D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





