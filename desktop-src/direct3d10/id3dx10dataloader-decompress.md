---
description: Используется для распаковки закодированных данных. Обычно это используется для загрузки ресурсов из файловых систем, таких как ZIP-файлы. При загрузке из несжатого ресурса стадия распаковки не должна выполнять никаких действий.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: 'ID3DX10DataLoader: метод:D екомпресс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c9e532bae8cb121fc93f3fdf2a5a1ee23e597c66599277b73b3b36b15ebbb963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989124"
---
# <a name="id3dx10dataloaderdecompress-method"></a>ID3DX10DataLoader: метод:D екомпресс

Используется для распаковки закодированных данных. Обычно это используется для загрузки ресурсов из файловых систем, таких как ZIP-файлы. При загрузке из несжатого ресурса стадия распаковки не должна выполнять никаких действий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдата* \[ заполняет\]
</dt> <dd>

Тип: **void \* \***

Указатель на необработанные данные для распаковки.

</dd> <dt>

*пкбитес* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***

Размер данных, на которые указывает Ппдата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

[**Интерфейс ID3DX10DataLoader**](id3dx10dataloader.md) может быть унаследован и его члены переопределяются. Распаковку можно переопределить для поддержки собственных пользовательских форматов файлов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
