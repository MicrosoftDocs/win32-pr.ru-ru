---
description: Возвращает список профилей DirectX Video Acceleration (ДКСВА), поддерживаемых драйвером экрана.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'Метод IDirect3DVideoDevice9:: Жетдксвагуидс (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 6a355c27177a546a2e91e769f72d9f4b9e216b005f711d42b5b7af39b4b78361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269244"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>Метод IDirect3DVideoDevice9:: Жетдксвагуидс

Возвращает список профилей DirectX Video Acceleration (ДКСВА), поддерживаемых драйвером экрана.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнумгуидс* 
</dt> <dd>

В поле входные данные указывает количество элементов в массиве *пгуидс* . Если *пгуидс* имеет **значение NULL**, значение `*pNumGuids` должно быть равно нулю.

В выходных данных, если *пгуидс* имеет **значение NULL**, *пнумгуидс* получает количество профилей дксва с ограниченным режимом. В противном случае *пнумгуидс* получает фактическое число идентификаторов GUID, копируемых в массив *пгуидс* .

</dd> <dt>

*пгуидс* 
</dt> <dd>

Адрес массива идентификаторов GUID или **значение NULL**. Если значение не **равно NULL**, массив получает список идентификаторов GUID, которые ОПРЕДЕЛЯЮТ профили дксва с ограниченным режимом. Эти идентификаторы GUID определены в дксва. h и описаны в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Вызовите этот метод дважды. При первом вызове задайте для *Пгуидс* **значение NULL**. Параметр *пнумгуидс* получает количество идентификаторов GUID для профиля дксва. Выделите массив идентификаторов GUID с требуемым размером и снова вызовите метод. На этот раз задайте *пгуидс* в качестве адреса массива. Метод заполняет массив списком идентификаторов GUID профиля ДКСВА.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 
