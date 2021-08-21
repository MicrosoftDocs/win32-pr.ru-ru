---
description: Получает идентификатор шаблона для этого узла файловых данных.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: 'Метод ID3DXFileSaveData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ec0dddd2106acddc5d09354ba7919eb32a8217a115410a9830803aaae589c891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987434"
---
# <a name="id3dxfilesavedatagettype-method"></a>Метод ID3DXFileSaveData:: GetType

Получает идентификатор шаблона для этого узла файловых данных.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тип* \[ окне\]
</dt> <dd>

Тип: **[ **GUID**](guid.md)\***

Указатель на идентификатор GUID, представляющий шаблон в этом узле данных файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадобжект, D3DXFERR \_ бадвалуе.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




