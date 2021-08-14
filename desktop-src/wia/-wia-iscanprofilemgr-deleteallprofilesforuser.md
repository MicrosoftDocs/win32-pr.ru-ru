---
description: Удаляет все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: 'Исканпрофилемгр: метод:D Елетеаллпрофилесфорусер (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 967a2ca3e2ed313c024f52cec6d8064c702c6caedc122ce7bd4409f3408ec995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209104"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a>Исканпрофилемгр: метод:D Елетеаллпрофилесфорусер

Удаляет все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофилемгр. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофилемгр**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




