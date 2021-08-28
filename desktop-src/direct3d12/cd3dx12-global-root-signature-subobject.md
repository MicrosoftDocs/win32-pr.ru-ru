---
title: Класс CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT (D3dx12. h)
description: Вспомогательный класс для создания глобального корневого состояния подписи субожект.
keywords:
- Класс CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 7ee327c24f5cc99fa386376be76ae0908fea19b6
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812483"
---
# <a name="cd3dx12_global_root_signature_subobject-class"></a>Класс CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT

Вспомогательный класс для создания глобального корневого состояния подписи субожект.

Дополнительные сведения о вспомогательных параметрах создания объектов состояния D3DX12 см. в разделе [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Синтаксис

```cpp
class CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT
{
    CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT() noexcept;
    CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetRootSignature(ID3D12RootSignature* pRootSig) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator ID3D12RootSignature* () const noexcept { return D3DX12_COM_PTR_GET(m_pRootSig); }
};
```

## <a name="members"></a>Члены

`CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT`

Конструктор по умолчанию. Создает новый экземпляр **CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT**, инициализированный по умолчанию.

`CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT** , инициализируемый с помощью содержимого объекта [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetRootSignature(ID3D12RootSignature*)`

Функция для установки корневой подписи в форме указателя на [ID3D12RootSignature](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) , переданный в качестве параметра.

`Type`

Возвращает тип подобъекта, представленного [D3D12_STATE_SUBOBJECT_TYPE_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) константой.

`operator const D3D12_STATE_SUBOBJECT&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) объект, описывающий объект состояния.

`operator ID3D12RootSignature*`

Оператор преобразования, возвращающий корневую подпись в виде указателя на [ID3D12RootSignature](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature).

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
