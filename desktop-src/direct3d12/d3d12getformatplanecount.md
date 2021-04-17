---
title: Функция D3D12GetFormatPlaneCount (D3dx12. h)
description: Возвращает число плоскостей для указанного формата DXGI для указанного виртуального адаптера (ID3D12Device).
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- Функция D3D12GetFormatPlaneCount
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703663"
---
# <a name="d3d12getformatplanecount-function"></a>Функция D3D12GetFormatPlaneCount

Возвращает число плоскостей для указанного формата DXGI для указанного виртуального адаптера ( **ID3D12Device**).

## <a name="syntax"></a>Синтаксис


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***

Виртуальный адаптер ( [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)), для которого необходимо получить число плоскостей.

</dd> <dt>

*Формат* 
</dt> <dd>

Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

[**\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , для которого необходимо получить число плоскостей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UINT8**

Количество плоскостей для указанного формата на указанном виртуальном адаптере.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ Сведения о формате данных компонента D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[Вспомогательные функции для D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

