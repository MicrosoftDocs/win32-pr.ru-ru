---
title: Класс CD3DX12_HIT_GROUP_SUBOBJECT (D3dx12. h)
description: Вспомогательный класс для создания подобъекта состояния группы попаданий.
keywords:
- Класс CD3DX12_HIT_GROUP_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_HIT_GROUP_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 68b95f15c41fd46bfaeb58943720d3b657a3208d9a0276e9ab65fe7bd6087c42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037387"
---
# <a name="cd3dx12_hit_group_subobject-class"></a>Класс CD3DX12_HIT_GROUP_SUBOBJECT

Вспомогательный класс для создания подобъекта состояния группы попаданий.

Дополнительные сведения о вспомогательных параметрах создания объектов состояния D3DX12 см. в разделе [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Синтаксис

```cpp
class CD3DX12_HIT_GROUP_SUBOBJECT
{
    CD3DX12_HIT_GROUP_SUBOBJECT() noexcept;
    CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetHitGroupExport(LPCWSTR exportName);
    void SetHitGroupType(D3D12_HIT_GROUP_TYPE Type) noexcept;
    void SetAnyHitShaderImport(LPCWSTR importName);
    void SetClosestHitShaderImport(LPCWSTR importName);
    void SetIntersectionShaderImport(LPCWSTR importName);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator const D3D12_HIT_GROUP_DESC& () const noexcept { return m_Desc; }
};
```

## <a name="members"></a>Члены

`CD3DX12_HIT_GROUP_SUBOBJECT`

Конструктор по умолчанию. Создает новый экземпляр **CD3DX12_HIT_GROUP_SUBOBJECT**, инициализированный по умолчанию.

`CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_HIT_GROUP_SUBOBJECT** , инициализируемый с помощью содержимого объекта [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetHitGroupExport(LPCWSTR)`

Функция для установки имени группы попаданий.

`SetHitGroupType(D3D12_HIT_GROUP_TYPE)`

Функция для установки значения из перечисления [D3D12_HIT_GROUP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type) , указывающего тип группы попаданий.

`SetAnyHitShaderImport(LPCWSTR)`

Функция для необязательного задания имени любого шейдера нажатия, связанного с группой попаданий.

`SetClosestHitShaderImport(LPCWSTR)`

Функция для необязательного задания имени шейдера нажатия, связанного с группой попаданий.

`SetIntersectionShaderImport(LPCWSTR)`

Функция для необязательного задания имени, связанного с группой попаданий, с необязательным именем шейдера пересечения.

`Type`

Возвращает тип подобъекта, представленного [D3D12_STATE_SUBOBJECT_TYPE_HIT_GROUP](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) константой.

`operator const D3D12_STATE_SUBOBJECT&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) объект, описывающий объект состояния.

`operator const D3D12_HIT_GROUP_DESC&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) объект, описывающий объект состояния.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также раздел

* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
