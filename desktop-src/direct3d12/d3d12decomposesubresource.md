---
title: Функция D3D12DecomposeSubresource (D3dx12.h)
description: Выводит срез MIP, срез массива и срез, соответствующие указанному индексу подресурса.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- Функция D3D12DecomposeSubresource
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c27089fb09c2408917be06b2f74e6d32f3e2f5aa9b96924de1ab92de190efb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045642"
---
# <a name="d3d12decomposesubresource-function"></a>Функция D3D12DecomposeSubresource

Выводит срез MIP, срез массива и срез, соответствующие указанному индексу подресурса.

## <a name="syntax"></a>Синтаксис


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Подресурс* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс подресурса.

</dd> <dt>

*миплевелс* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Максимальное число уровней mipmap в подресурсе.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Количество элементов в массиве.

</dd> <dt>

*Мипслице* \[ out, ref\]
</dt> <dd>

Тип: **T**

Выводит срез MIP, соответствующий заданному индексу подресурса.

</dd> <dt>

*Аррайслице* \[ out, ref\]
</dt> <dd>

Тип: **U**

Выводит срез массива, соответствующий заданному индексу подресурса.

</dd> <dt>

*Планеслице* \[ out, ref\]
</dt> <dd>

Тип: **V**

Выводит срез плоскости, соответствующий заданному индексу подресурса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Эта функция определяет, какой срез MIP, срез массива и срез плоскости соответствуют заданному индексу подресурсов. Это полезная служебная программа, хотя это и зависит от языка C++.

Эта функция объявляется следующим образом с параметрами C++ преобразованный для типов **T**, **U** и **V**:


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также

[Вспомогательные функции для D3D12](helper-functions-for-d3d12.md)

[Подресурсы](subresources.md)
