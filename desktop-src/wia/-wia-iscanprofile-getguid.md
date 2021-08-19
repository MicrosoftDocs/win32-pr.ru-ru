---
description: Возвращает идентификатор GUID профиля.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: Метод Исканпрофиле::-GUID (Сканпрофиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 37d383d5975957c45b2aa5a0c90350f794e6f20deb9a7bfbe73c9f2d42b2bca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441582"
---
# <a name="iscanprofilegetguid-method"></a>Метод Исканпрофиле::

Возвращает идентификатор GUID профиля.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*retval* \[ заполняет\]
</dt> <dd>

Тип: **GUID \***

Указатель на идентификатор GUID профиля.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Идентификатор GUID для профиля создается автоматически при создании профиля с помощью [**креатепрофиле**](-wia-iscanprofilemgr-createprofile.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




