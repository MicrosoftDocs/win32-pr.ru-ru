---
description: Создает пустой профиль сканирования и связывает его с сканером или другим элементом для получения изображения Windows (WIA) 2,0.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'Метод Исканпрофилемгр:: Креатепрофиле (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497724"
---
# <a name="iscanprofilemgrcreateprofile-method"></a>Метод Исканпрофилемгр:: Креатепрофиле

Создает пустой профиль сканирования и связывает его с сканером или другим элементом для получения изображения Windows (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрдевицеид* \[ окне\]
</dt> <dd>

Тип: **BSTR**

ИДЕНТИФИКАТОР устройства или элемента WIA 2,0.

</dd> <dt>

*bstrName* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Понятное имя нового профиля.

</dd> <dt>

*гуидкатегори* \[ окне\]
</dt> <dd>

Тип: **GUID**

Идентификатор GUID категории для устройства или элемента WIA 2,0. Это должна быть одна из \_ \_ констант категории элемента WIA IPA \_ .

</dd> <dt>

*ппсканпрофиле* \[ заполняет\]
</dt> <dd>

Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\*\***

Адрес указателя на новый профиль.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

**Исканпрофилемгр:: креатепрофиле** связывает указанное устройство с новым профилем сканирования.

**Исканпрофилемгр:: креатепрофиле** автоматически создает идентификатор GUID для нового профиля. Получите [**GUID с помощью**](-wia-iscanprofile-getguid.md).

Используйте метод [**исканпрофилемгр:: Refresh**](-wia-iscanprofilemgr-refresh.md) , если несколько объектов [**исканпрофилемгр**](-wia-iscanprofilemgr.md) могут создавать или удалять профили одновременно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофилемгр. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофилемгр**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




