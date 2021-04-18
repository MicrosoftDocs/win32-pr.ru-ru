---
title: Функция Коммандлисткаст (D3dx12. h)
description: Этот шаблон функции приводит указатель константы к любому списку команд в указатель const на ID3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- Функция Коммандлисткаст
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713927"
---
# <a name="commandlistcast-function"></a>Функция Коммандлисткаст

Этот шаблон функции приводит указатель константы к любому списку команд в указатель const на ID3D12CommandList.

Это приведение полезно для передачи строго типизированных указателей списка команд в [**ексекутекоммандлистс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="syntax"></a>Синтаксис


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PP* 
</dt> <dd>

Тип: **t \_ коммандлисттипе \* const \***

Строго типизированный список команд для приведения.

Аргумент шаблона **t \_ коммандлисттипе** указывает любой строго типизированный объект списка команд.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **ID3D12CommandList \* const \***

Строго типизированный список команд, повторно интерпретируемый как [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).

## <a name="remarks"></a>Комментарии

Коммандлисткаст выполняет **переинтерпретируемое \_ приведение**. Приведение допустимо, пока учитывается константа-rvalue характеристики списка команд.

Функция Коммандлисткаст определяется следующим образом:


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные функции для D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





