---
description: Извлекает имя этого файлового объекта данных.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: Метод ID3DXFileData::-Name (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713802"
---
# <a name="id3dxfiledatagetname-method"></a>Метод ID3DXFileData:: Name

Извлекает имя этого файлового объекта данных.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*szName* \[ окне\]
</dt> <dd>

Тип: **[ **LPSTR**](../winprog/windows-data-types.md)**

Адрес указателя для получения имени этого файлового объекта данных. Если этот параметр имеет **значение NULL**, пуисизе будет возвращать размер строки. Если параметр szName указывает на допустимую память, имя этого файлового объекта данных будет скопировано в объект szName до количества символов, заданного параметром Пуисизе.

</dd> <dt>

*пуисизе* \[ в, out\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***

Указатель на размер строки, представляющей имя этого объекта файловых данных. Этот параметр может иметь **значение NULL** , если szName предоставляет ссылку на имя. Этот параметр возвращает размер строки, если параметр szName имеет **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.

## <a name="remarks"></a>Комментарии

Чтобы этот метод был выполнен, параметр szName или *пуисизе* должен иметь значение, отличное от **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
