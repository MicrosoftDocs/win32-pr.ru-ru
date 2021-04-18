---
description: Возвращает число профилей сканирования, созданных для пользователя в системе, в которой выполняется приложение.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'Метод Исканпрофилемгр:: Жетнумпрофилес (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702225"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a>Метод Исканпрофилемгр:: Жетнумпрофилес

Возвращает число профилей сканирования, созданных для пользователя в системе, в которой выполняется приложение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулнумпрофилес* \[ заполняет\]
</dt> <dd>

Тип: **ulong \** _

Указатель на число профилей, созданных для пользователя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

 

 




