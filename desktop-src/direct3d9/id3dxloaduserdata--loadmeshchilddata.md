---
description: Загрузка дочерних данных сетки из файла. x.
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: 'Метод ID3DXLoadUserData:: Лоадмешчилддата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9960f47ac21dad2521f6272c9176e3d895bbd109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713562"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a>Метод ID3DXLoadUserData:: Лоадмешчилддата

Загрузка дочерних данных сетки из файла. x.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмешконтаинер* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

Указатель на контейнер сетки. См. [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

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
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




