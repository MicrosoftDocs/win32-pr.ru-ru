---
title: Класс CD3DX12_EXISTING_COLLECTION_SUBOBJECT (D3dx12. h)
description: Вспомогательный класс для создания существующего вложенного объекта состояния коллекции.
keywords:
- Класс CD3DX12_EXISTING_COLLECTION_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_EXISTING_COLLECTION_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 2059bca83236ae51cbd69a9480624c3e540f18d6
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813289"
---
# <a name="cd3dx12_existing_collection_subobject-class"></a>Класс CD3DX12_EXISTING_COLLECTION_SUBOBJECT

Вспомогательный класс для создания существующего вложенного объекта состояния коллекции.

Дополнительные сведения о вспомогательных параметрах создания объектов состояния D3DX12 см. в разделе [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Синтаксис

```cpp
class CD3DX12_EXISTING_COLLECTION_SUBOBJECT
{
    CD3DX12_EXISTING_COLLECTION_SUBOBJECT() noexcept;
    CD3DX12_EXISTING_COLLECTION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&);
    SetExistingCollection(ID3D12StateObject* pExistingCollection) noexcept;
    void DefineExport(
        LPCWSTR Name,
        LPCWSTR ExportToRename = nullptr,
        D3D12_EXPORT_FLAGS Flags = D3D12_EXPORT_FLAG_NONE);
    template<size_t N> void DefineExports(LPCWSTR(&Exports)[N]);
    void DefineExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_EXISTING_COLLECTION_DESC& () const noexcept;
};
```

## <a name="members"></a>Члены

`CD3DX12_EXISTING_COLLECTION_SUBOBJECT`

Конструктор по умолчанию. Создает новый экземпляр **CD3DX12_EXISTING_COLLECTION_SUBOBJECT**, инициализированный по умолчанию.

`CD3DX12_EXISTING_COLLECTION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_EXISTING_COLLECTION_SUBOBJECT** , инициализируемый с помощью содержимого объекта [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetExistingCollection(ID3D12StateObject*)`

Функция для установки существующей коллекции в форме указателя на [ID3D12StateObject](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) , переданный в качестве параметра.

`DefineExport(LPCWSTR, LPCWSTR = nullptr, D3D12_EXPORT_FLAGS)`

Определяет символ, экспортированный из подобъекта. Принимает [D3D12_EXPORT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_export_flags) в качестве необязательного параметра.

`DefineExports(LPCWSTR(&)[N]);`

Определяет массив символов, экспортированных из подобъекта. Параметр шаблона *N* указывает количество элементов в массиве.

`DefineExports(const LPCWSTR*, UINT)`

Определяет массив из *N* символов, экспортированных из подобъекта.

`Type`

Возвращает тип подобъекта, представленного [D3D12_STATE_SUBOBJECT_TYPE_EXISTING_COLLECTION](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) константой.

`operator const D3D12_STATE_SUBOBJECT&`

Оператор преобразования, возвращающий ссылку на константу [**D3D12_STATE_SUBOBJECT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) объект, описывающий объект состояния.

`operator const D3D12_EXISTING_COLLECTION_DESC&`

Оператор преобразования, возвращающий ссылку на константу [**D3D12_EXISTING_COLLECTION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_existing_collection_desc) объект, описывающий объект состояния.

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
