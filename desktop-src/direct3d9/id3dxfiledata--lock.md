---
description: Обращается к данным файла. x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'Метод ID3DXFileData:: Lock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c052f570b3206c5a0661a4cf4ab38b259fb476f4eda1322df80e709608d09bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520711"
---
# <a name="id3dxfiledatalock-method"></a>Метод ID3DXFileData:: Lock

Обращается к данным файла. x.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псизе* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***

Указатель на размер данных файла. x.

</dd> <dt>

*ппдата* \[ окне\]
</dt> <dd>

Тип: **константа \* \* void**

Адрес указателя для получения указателя интерфейса объекта данных [**ID3DXFileData**](id3dxfiledata.md) File. См. заметки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.

## <a name="remarks"></a>Remarks

Указатель *ппдата* допустим только во время **ID3DXFileData:: Lock** ... Последовательность [**ID3DXFileData:: Unlock**](id3dxfiledata--unlock.md) . Можно выполнить несколько вызовов блокировок. Однако необходимо убедиться, что количество вызовов блокировок соответствует числу вызовов Unlock.

Так как данные файлов не гарантированно правильно согласованы с границами байтов, доступ к *ппдата* должен осуществляться с помощью несогласованных указателей.

Возвращаемые значения параметров не обязательно должны быть допустимы из-за возможного повреждения файла; Поэтому код должен проверять возвращаемые значения параметров.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
