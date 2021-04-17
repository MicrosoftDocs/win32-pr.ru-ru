---
description: Определяет данные анимации сжатых ключевых кадров.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Структура КСФИЛЕКОМПРЕССЕДАНИМАТИОНСЕТ (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684984"
---
# <a name="xfilecompressedanimationset-structure"></a>Структура КСФИЛЕКОМПРЕССЕДАНИМАТИОНСЕТ

Определяет данные анимации сжатых ключевых кадров.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a>Члены

<dl> <dt>

**компресседблокксизе**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Общий размер (в байтах) сжатых данных в буфере данных анимации сжатого опорного кадра.

</dd> <dt>

**тикксперсек**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Число тактов кадра анимации, которые находятся в секунду.

</dd> <dt>

**плайбакктипе**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Тип цикла воспроизведения набора анимации. См. раздел [**\_ тип D3DXPLAYBACK**](./d3dxplayback-type.md).

</dd> <dt>

**BufferLength**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Минимальный размер буфера (в байтах), необходимый для хранения данных анимации с сжатыми ключевыми кадрами. Значение равно ((Компресседблокксизе + 3)/4).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры файлов D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
