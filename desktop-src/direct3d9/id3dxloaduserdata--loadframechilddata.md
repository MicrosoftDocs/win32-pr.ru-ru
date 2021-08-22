---
description: Загрузка дочерних данных фрейма из файла. x.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: 'Метод ID3DXLoadUserData:: Лоадфрамечилддата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3dcb9fa8218804b0d6fdb5532dd54bc2b2b4a3921ea4462692a36e671efb404d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802184"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a>Метод ID3DXLoadUserData:: Лоадфрамечилддата

Загрузка дочерних данных фрейма из файла. x.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфраме* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**

Указатель на контейнер сетки. См. [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*пксофчилддата* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Указатель на структуру данных файла. x. Это определено в Дксфиле. h.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемые значения этого метода реализуются программистом приложения. Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК. В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от D3DERR или D3DXERR, так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




