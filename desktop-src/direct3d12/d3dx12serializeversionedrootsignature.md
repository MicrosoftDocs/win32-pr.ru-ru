---
title: Функция D3DX12SerializeVersionedRootSignature (D3dx12. h)
description: Помогает включить функции корневой подписи 1,1, когда они доступны, и не требует поддержки двух путей кода для сборки корневых подписей. Этот вспомогательный метод восстанавливает корневую подпись версии 1,0, если версия 1,1 не поддерживается.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- Функция D3DX12SerializeVersionedRootSignature
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703658"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a>Функция D3DX12SerializeVersionedRootSignature

Помогает включить функции корневой подписи 1,1, когда они доступны, и не требует поддержки двух путей кода для сборки корневых подписей. Этот вспомогательный метод восстанавливает корневую подпись версии 1,0, если версия 1,1 не поддерживается.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прутсигнатуредеск* \[ окне\]
</dt> <dd>

Тип: **const D3D12 с \_ версией \_ корневая \_ подпись \_ DESC \***

Указывает [**D3D12 \_ \_ корневую \_ подпись \_ с версией**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) , которая содержит описание любой версии корневой подписи.

</dd> <dt>

*MaxVersion* 
</dt> <dd>

Тип: **\_ версия " \_ корневая \_ сигнатура D3D** "

Указывает максимальную поддерживаемую [**\_ версию для корневой \_ сигнатуры \_ D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).

</dd> <dt>

*ппблоб* \[ заполняет\]
</dt> <dd>

Тип: **ID3DBlob \* \***

Указатель на блок памяти, который получает указатель на интерфейс [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) , который можно использовать для доступа к сериализованной корневой подписи.

</dd> <dt>

*пперрорблоб* \[ out, необязательно\]
</dt> <dd>

Тип: **ID3DBlob \* \***

Указатель на блок памяти, который получает указатель на интерфейс [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) , который можно использовать для доступа к сообщениям об ошибках сериализатора, или **значение NULL** , если ошибок нет.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает **значение \_ ОК** , если выполнено успешно; в противном случае возвращает один из [кодов возврата Direct3D 12](d3d12-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Комментарии

Эта функция была выпущена и совпадает с годовщиной обновления Windows 10 (14393). Для поддержки версий Windows 10 до этого для использования этой функции требуется настроить d3d12. lib для *отложенной загрузки*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[Вспомогательные функции для D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

