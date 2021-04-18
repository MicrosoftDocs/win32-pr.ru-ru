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
ms.openlocfilehash: b774f71b4be111efcdbdaf8bc41b40d4b0efaa95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694305"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




