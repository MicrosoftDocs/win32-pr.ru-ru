---
description: Извлекает идентификатор GUID для этого узла данных файла ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'Метод ID3DXFileSaveData:: GetId (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b03322e03d1bedc10f9deec82c60418b5ad846b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694226"
---
# <a name="id3dxfilesavedatagetid-method"></a>Метод ID3DXFileSaveData:: GetId

Извлекает идентификатор GUID для этого узла данных файла [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор процесса* \[ заполняет\]
</dt> <dd>

Тип: **лпгуид**

Указатель на GUID, получающий идентификатор этого узла файловых данных. Если у объекта нет идентификатора, возвращаемое значение параметра будет \_ равно GUID null.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




