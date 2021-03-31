---
description: Создает экземпляр объекта ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: Функция D3DXFileCreate (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157187"
---
# <a name="d3dxfilecreate-function"></a>Функция D3DXFileCreate

Создает экземпляр объекта [**ID3DXFile**](id3dxfile.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лплпдиректксфиле* 
</dt> <dd>

Тип: **[ **ID3DXFile**](id3dxfile.md)\*\***

Адрес указателя на интерфейс [**ID3DXFile**](id3dxfile.md) , представляющий созданный объект файла. x.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: \_ указатель e, e \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

После использования этой функции используйте [**регистертемплатес**](id3dxfile--registertemplates.md) или [**регистеренумтемплатес**](id3dxfile--registerenumtemplates.md) для регистрации шаблонов, [**креатинумобжект**](id3dxfile--createenumobject.md) для создания объекта перечислителя или [**креатесавеобжект**](id3dxfile--createsaveobject.md) для создания объекта Save.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции файла D3DX X](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[**креатинумобжект**](id3dxfile--createenumobject.md)
</dt> <dt>

[**креатесавеобжект**](id3dxfile--createsaveobject.md)
</dt> <dt>

[**регистеренумтемплатес**](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[**регистертемплатес**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




