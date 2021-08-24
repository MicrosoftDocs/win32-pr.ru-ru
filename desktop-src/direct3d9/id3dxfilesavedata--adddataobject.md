---
description: Добавляет объект данных в качестве дочернего элемента для узла данных файла ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'Метод ID3DXFileSaveData:: Адддатаобжект (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ed4b0abd35f9f53fb2111f40903e4b2b81a75c9d402a53fbb2fdb1cdc9a75750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847844"
---
# <a name="id3dxfilesavedataadddataobject-method"></a>Метод ID3DXFileSaveData:: Адддатаобжект

Добавляет объект данных в качестве дочернего элемента для узла данных файла [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

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

Указатель на имя добавляемого объекта данных. Укажите **значение NULL** , если у объекта нет имени.

</dd> <dt>

*идентификатор процесса* \[ окне\]
</dt> <dd>

Тип: **константа [**GUID**](guid.md) \***

Указатель на идентификатор GUID, представляющий объект данных. Объект данных должен быть зарегистрирован с помощью [**ID3DXFile:: регистертемплатес**](id3dxfile--registertemplates.md) или [**ID3DXFile:: регистеренумтемплатес**](id3dxfile--registerenumtemplates.md). Укажите **значение NULL** , если у объекта нет идентификатора GUID.

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

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадобжект, D3DXFERR \_ Бадвалуе, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
