---
title: Класс CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT (D3dx12. h)
description: Вспомогательный класс для создания подобъекта состояния конфигурации райтраЦинг Shader.
keywords:
- Класс CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 69f30a3cae1eeab030c8929ccd606fb892f27dd5
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812919"
---
# <a name="cd3dx12_raytracing_shader_config_subobject-class"></a>Класс CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT

Вспомогательный класс для создания подобъекта состояния конфигурации райтраЦинг Shader.

Дополнительные сведения о вспомогательных параметрах создания объектов состояния D3DX12 см. в разделе [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Синтаксис

```cpp
class CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT
{
    CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void Config(UINT MaxPayloadSizeInBytes, UINT MaxAttributeSizeInBytes) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_RAYTRACING_SHADER_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Члены

`CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT`

Конструктор по умолчанию. Создает новый экземпляр **CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT**, инициализированный по умолчанию.

`CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT** , инициализируемый с помощью содержимого объекта [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`Config(UINT, UINT)`

Функция для настройки максимального размера полезных данных и максимальный размер атрибута (в байтах).

`Type`

Возвращает тип подобъекта, представленного [D3D12_STATE_SUBOBJECT_TYPE_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) константой.

`operator const D3D12_STATE_SUBOBJECT&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) объект, описывающий объект состояния.

`operator const D3D12_RAYTRACING_SHADER_CONFIG&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) объект, описывающий объект состояния.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
