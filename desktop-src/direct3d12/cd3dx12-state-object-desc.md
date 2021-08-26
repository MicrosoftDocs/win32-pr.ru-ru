---
title: Класс CD3DX12_STATE_OBJECT_DESC (D3dx12. h)
description: Центральный класс вспомогательных функций создания объектов состояния D3DX12, которые представляют собой вспомогательные классы для создания объектов состояния из произвольного набора подобъектов.
keywords:
- Класс CD3DX12_STATE_OBJECT_DESC
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: cc3d65a9779c379debd94e7872717e4449a71ac8
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813080"
---
# <a name="cd3dx12_state_object_desc-class"></a>Класс CD3DX12_STATE_OBJECT_DESC

Центральный класс вспомогательных функций создания объектов состояния D3DX12, которые представляют собой вспомогательные классы для создания объектов состояния из произвольного набора подобъектов.

## <a name="syntax"></a>Синтаксис

```cpp
class CD3DX12_STATE_OBJECT_DESC
{
    CD3DX12_STATE_OBJECT_DESC() noexcept;
    CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE) noexcept;
    void SetStateObjectType(D3D12_STATE_OBJECT_TYPE) noexcept;
    operator const D3D12_STATE_OBJECT_DESC& ();
    operator const D3D12_STATE_OBJECT_DESC* ();
    template<typename T> T* CreateSubobject();
};
```

## <a name="members"></a>Члены

`CD3DX12_STATE_OBJECT_DESC`

Конструктор по умолчанию. Создает новый экземпляр **CD3DX12_STATE_OBJECT_DESC**, инициализированный по умолчанию.

`CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE)`

Конструктор, создающий новый экземпляр **CD3DX12_STATE_OBJECT_DESC** , инициализируемый типом субжобжект, соответствующим значению переданного ему [**D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) .

`SetStateObjectType(D3D12_STATE_OBJECT_TYPE)`

, Который задает для типа субжобжект значение переданного ему [**D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) .

`operator const D3D12_STATE_OBJECT_DESC&`

Оператор преобразования, возвращающий ссылку на константу [**D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) объект, описывающий объект состояния.

`operator const D3D12_STATE_OBJECT_DESC*`

Оператор преобразования, возвращающий указатель на константу [**D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) объекта, описывающего объект состояния.

`CreateSubobject`

Шаблон функции, создающий вспомогательный метод субубжект, время существования которого принадлежит этому классу.

Параметр шаблона *T* указывает тип вспомогательного метода субжобжект, например [CD3DX12_HIT_GROUP_SUBOBJECT](cd3dx12-hit-group-subobject.md).

## <a name="remarks"></a>Remarks

Чтобы использовать вспомогательные методы для создания объектов состояния D3DX12, начните с создания экземпляра объекта **CD3DX12_STATE_OBJECT_DESC** и вызовите его функцию **креатесубобжект** для создания подобъектов. Каждый вспомогательный объект содержит методы, специфичные для этого подобъекта, для настройки его содержимого.

```cpp
CD3DX12_STATE_OBJECT_DESC Collection1(D3D12_STATE_OBJECT_TYPE_COLLECTION);
auto Lib0 = Collection1.CreateSubobject<CD3DX12_DXIL_LIBRARY_SUBOBJECT>();
Lib0->SetDXILLibrary(&pMyAppDxilLibs[0]);
Lib0->DefineExport(L"rayGenShader0");
// In practice, these export listings might be data/engine-driven.
...
```

Кроме того, можно явно создать экземпляры вспомогательных функций для вспомогательных объектов, например, с помощью локальных переменных, передав объект состояния desc (который должен указывать на него) в конструктор (или вызов `mySubobjectHelper.AddToStateObject(Collection1)` ).

В этом альтернативном сценарии необходимо обеспечить активность подобъекта до тех пор, пока объект состояния, с которым он связан, является активным, в противном случае ссылки на его указатели будут устаревшими.

```cpp
CD3DX12_STATE_OBJECT_DESC RaytracingState2(D3D12_STATE_OBJECT_TYPE_RAYTRACING_PIPELINE);
CD3DX12_DXIL_LIBRARY_SUBOBJECT LibA(RaytracingState2);
LibA.SetDXILLibrary(&pMyAppDxilLibs[4]);
// Not manually specifying exports; meaning that all exports in the libraries are exported.
...
```

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
