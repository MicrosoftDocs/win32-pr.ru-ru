---
description: Добавляет ссылку на данные в качестве дочернего элемента для этого узла данных ID3DXFileSaveData File. Ссылка на данные указывает на объект данных файла.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'Метод ID3DXFileSaveData:: Адддатареференце (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 862df88701cffd1059ca67e086cd49d05174bc66e9fa13807df2d2aeb0c9ff1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121353"
---
# <a name="id3dxfilesavedataadddatareference-method"></a>Метод ID3DXFileSaveData:: Адддатареференце

Добавляет ссылку на данные в качестве дочернего элемента для этого узла данных [**ID3DXFileSaveData**](id3dxfilesavedata.md) File. Ссылка на данные указывает на объект данных файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*szName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на имя объекта данных, который необходимо добавить по ссылке. Укажите **значение NULL** , если у объекта данных нет имени.

</dd> <dt>

*идентификатор процесса* \[ окне\]
</dt> <dd>

Тип: **константа [**GUID**](guid.md) \***

Указатель на идентификатор GUID, представляющий объект данных, который необходимо добавить по ссылке. Если **значение равно NULL**, будет добавлена ссылка, указывающая на объект данных с именем, заданным параметром szName.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадобжект, D3DXFERR \_ Бадвалуе, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Объект данных файла, на который указывает ссылка, должен иметь либо имя, либо идентификатор GUID. Объект данных файла также должен быть производным от другого родительского объекта [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
