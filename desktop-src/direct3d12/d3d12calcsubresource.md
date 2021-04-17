---
title: Функция D3D12CalcSubresource (D3dx12. h)
description: Вычисляет индекс подресурсов для текстуры.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- Функция D3D12CalcSubresource
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703664"
---
# <a name="d3d12calcsubresource-function"></a>Функция D3D12CalcSubresource

Вычисляет индекс подресурсов для текстуры.

## <a name="syntax"></a>Синтаксис


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*мипслице* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый от нуля индекс для адреса уровня mipmap. 0 означает первый, наиболее подробный уровень mipmap.

</dd> <dt>

*аррайслице* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый от нуля индекс для уровня массива, по которому производится адресация; всегда используйте 0 для 3D-текстур.

</dd> <dt>

*планеслице* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый от нуля индекс для уровня плоскости, по которому производится адресация.

</dd> <dt>

*миплевелс* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число уровней mipmap в ресурсе.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Количество элементов в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс, который равен Мипслице + (Аррайслице \* миплевелс).

## <a name="remarks"></a>Комментарии

Буфер является неструктурированным ресурсом и, следовательно, определяется как содержащий один подресурс. Для интерфейсов API, которые принимают буферы, не требуется индекс подресурса. Текстура с другой стороны очень структурирована. Каждый объект текстуры может содержать один или несколько подресурсов в зависимости от размера массива и количества mipmap уровней.

Для томов (трехмерных) все срезы для данного уровня mipmap являются одним индексом подресурса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные функции для D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Подресурсы](subresources.md)
</dt> </dl>

 

