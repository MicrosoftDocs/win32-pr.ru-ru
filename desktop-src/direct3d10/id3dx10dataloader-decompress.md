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
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694173"
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

## <a name="remarks"></a>Комментарии

[**Интерфейс ID3DX10DataLoader**](id3dx10dataloader.md) может быть унаследован и его члены переопределяются. Распаковку можно переопределить для поддержки собственных пользовательских форматов файлов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
