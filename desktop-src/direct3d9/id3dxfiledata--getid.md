---
description: Извлекает идентификатор GUID для этого файлового объекта данных.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'Метод ID3DXFileData:: GetId (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a9a1cbf98792b0ac36c35aabf40b8c125a497201b27c6a161c0706f077ffc491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295330"
---
# <a name="id3dxfiledatagetid-method"></a>Метод ID3DXFileData:: GetId

Извлекает идентификатор GUID для этого файлового объекта данных.

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

Указатель на идентификатор GUID для получения идентификатора этого объекта файловых данных. Если объект данных файла не имеет идентификатора, возвращаемое значение параметра будет \_ равно GUID null.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




