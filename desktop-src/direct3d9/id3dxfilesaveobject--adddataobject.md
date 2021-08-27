---
description: Добавляет объект данных в качестве дочернего элемента для объекта ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'Метод ID3DXFileSaveObject:: Адддатаобжект (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8a1bdea820b90ae68c819ae2755f2abecd892cfd362116f6da37cb643a254048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802419"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a>Метод ID3DXFileSaveObject:: Адддатаобжект

Добавляет объект данных в качестве дочернего элемента для объекта [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ргуидтемплате* \[ окне\]
</dt> <dd>

Тип: **[рефгуид](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Идентификатор GUID, представляющий шаблон объекта данных.

</dd> <dt>

*szName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на имя объекта данных. Укажите **значение NULL** , если у объекта нет имени.

</dd> <dt>

*идентификатор процесса* \[ окне\]
</dt> <dd>

Тип: **константа [**GUID**](guid.md) \***

Указатель на идентификатор GUID, представляющий объект данных. Укажите **значение NULL** , если у объекта нет идентификатора GUID.

</dd> <dt>

*кбсизе* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)**

Размер объекта данных в байтах.

</dd> <dt>

*пвдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на буфер, содержащий все необходимые данные в объекте данных.

</dd> <dt>

*ппобж* \[ в, retval\]
</dt> <dd>

Тип: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

Адрес указателя на интерфейс [**ID3DXFileSaveData**](id3dxfilesavedata.md) , представляющий узел данных файла, в который будет добавлен объект данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадобжект, дксфилирр \_ Бадвалуе, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Если эталонный объект данных будет ссылаться на объект данных, параметр szName или pId должен иметь значение, отличное от **null**.

Сохраните созданные данные на диск с помощью метода [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 
