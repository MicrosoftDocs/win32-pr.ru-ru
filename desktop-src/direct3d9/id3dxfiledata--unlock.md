---
description: 'Завершает срок существования указателя Ппдата, возвращенного ID3DXFileData:: Lock.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'Метод ID3DXFileData:: Unlock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821212"
---
# <a name="id3dxfiledataunlock-method"></a>Метод ID3DXFileData:: Unlock

Завершает срок существования указателя *ппдата* , возвращенного [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).

## <a name="syntax"></a>Синтаксис


```C++
BOOL Unlock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Возвращаемое значение — S \_ .

## <a name="remarks"></a>Комментарии

Необходимо убедиться, что число вызовов [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md) соответствует числу вызовов **ID3DXFileData:: Unlock** . После вызова функции Unlock указатель Ппдата, возвращенный **ID3DXFileData:: Lock** , больше не должен использоваться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
