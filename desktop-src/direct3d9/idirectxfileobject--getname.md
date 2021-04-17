---
description: Получает указатель на имя объекта файла DirectX. Не рекомендуется.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: Метод Идиректксфилеобжект::-Name (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684991"
---
# <a name="idirectxfileobjectgetname-method"></a>Метод Идиректксфилеобжект:: Name

Получает указатель на имя объекта файла DirectX. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстрнамебуф* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPSTR**](../winprog/windows-data-types.md)**

Указатель на буфер, в который будет скопировано имя объекта файла DirectX. Задайте **значение NULL** , если требуется только длина буфера.

</dd> <dt>

*пдвбуфлен* \[ в, out\]
</dt> <dd>

Тип: **[ **лпдворд**](../winprog/windows-data-types.md)**

Указатель на DWORD, указывающий длину буфера, на который указывает Пстрнамебуф. Значение параметра Пдвбуфлен будет изменено на длину буфера, необходимую для хранения имени объекта, даже если Пстрнамебуф имеет **значение NULL**. В любом случае функция возвратит ДКСФИЛИРР \_ бадвалуе, если исходное значение пдвбуфлен не превышает длину, необходимую для хранения имени объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений. ДКСФИЛИРР \_ БАДАЛЛОК дксфилирр \_ бадвалуе

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфилеобжект](idirectxfileobject.md)
</dt> </dl>

 

 
