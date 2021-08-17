---
description: Отмена сопоставления буфера.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'Метод ID3DX10MeshBuffer:: unотмена (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62b056b80b5722ce9173a7ca30200ba208cf88cf51c18d52b2a895d975121671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736043"
---
# <a name="id3dx10meshbufferunmap-method"></a>Метод ID3DX10MeshBuffer:: unотмена

Отмена сопоставления буфера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Unmap();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks



Различия между Direct3D 9 и Direct3D 10:

- Отмена сопоставления () в Direct3D 10 аналогична разблокировке ресурсов () в Direct3D 9.



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




