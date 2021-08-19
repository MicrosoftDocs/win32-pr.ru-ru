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
ms.openlocfilehash: 41c64ae7bb2ca4acf87e1b63de90f2ccfc78e8d769adf334aa1f68b9bf79de0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518570"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры файлов D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
