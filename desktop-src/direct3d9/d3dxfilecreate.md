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
ms.openlocfilehash: ccafd6e3cffb71cccbdf3025ead6ad2cc012f4d62ecf52405cf82dcda06a1531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849794"
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

## <a name="remarks"></a>Remarks

После использования этой функции используйте [**регистертемплатес**](id3dxfile--registertemplates.md) или [**регистеренумтемплатес**](id3dxfile--registerenumtemplates.md) для регистрации шаблонов, [**креатинумобжект**](id3dxfile--createenumobject.md) для создания объекта перечислителя или [**креатесавеобжект**](id3dxfile--createsaveobject.md) для создания объекта Save.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

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

 

 




