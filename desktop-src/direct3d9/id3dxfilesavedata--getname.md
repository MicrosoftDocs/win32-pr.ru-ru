---
description: Извлекает имя этого узла данных файла ID3DXFileSaveData.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: Метод ID3DXFileSaveData::-Name (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7aa6ef69a5296830b2f3bb992fb24ac23fa58adeeea629fd0e1bdeacf6173344
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856653"
---
# <a name="id3dxfilesavedatagetname-method"></a>Метод ID3DXFileSaveData:: Name

Извлекает имя этого узла данных файла [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

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

Адрес указателя для получения имени этого узла файловых данных. Если этот параметр имеет **значение NULL**, *пуисизе* будет возвращать размер строки. Если параметр szName указывает на действительную память, имя этого узла данных файла будет скопировано в параметр szName вплоть до количества символов, заданного *пуисизе* .

</dd> <dt>

*пуисизе* \[ в, out\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***

Указатель на размер строки, представляющей имя этого узла файловых данных. Этот параметр может иметь **значение NULL** , если szName предоставляет ссылку на имя. Этот параметр возвращает размер строки, если параметр szName имеет **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.

## <a name="remarks"></a>Remarks

Чтобы этот метод был выполнен, параметр *szName* или *Пуисизе* должен иметь значение, отличное от **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
