---
description: Интерфейс Исканпрофилемгр предоставляет методы для создания, открытия, удаления профилей сканирования и управления ими.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Интерфейс Исканпрофилемгр (Сканпрофилемгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662587"
---
# <a name="iscanprofilemgr-interface"></a>Интерфейс Исканпрофилемгр

Интерфейс **исканпрофилемгр** предоставляет методы для создания, открытия, удаления профилей сканирования и управления ими.

## <a name="members"></a>Элементы

Интерфейс **исканпрофилемгр** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Исканпрофилемгр** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **исканпрофилемгр** содержит следующие методы.



| Метод                                                                              | Описание                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**креатепрофиле**](-wia-iscanprofilemgr-createprofile.md)                         | Создает пустой профиль сканирования и связывает его с сканером или другим элементом WIA 2,0.<br/>                       |
| [**делетеаллпрофилес**](-wia-iscanprofilemgr-deleteallprofiles.md)                 | Удаляет все профили сканирования, связанные с указанным устройством.<br/>                                         |
| [**делетеаллпрофилесфорусер**](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | Удаляет все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение. <br/> |
| [**делетепрофиле**](-wia-iscanprofilemgr-deleteprofile.md)                         | Удаляет указанный профиль сканирования.<br/>                                                                         |
| [**жетдефаултпрофиле**](-wia-iscanprofilemgr-getdefaultprofile.md)                 | Возвращает профиль сканирования по умолчанию.<br/>                                                                              |
| [**жетнумпрофилес**](-wia-iscanprofilemgr-getnumprofiles.md)                       | Возвращает число профилей сканирования, созданных для пользователя в системе, в которой выполняется приложение.<br/> |
| [**жетнумпрофилесфордевицеид**](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | Возвращает число профилей сканирования для устройства.<br/>                                                            |
| [**Профили профилирования**](-wia-iscanprofilemgr-getprofiles.md)                             | Получает все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.<br/>     |
| [**жетпрофилесфордевицеид**](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | Возвращает все профили сканирования, связанные с устройством.<br/>                                                        |
| [**опенпрофиле**](-wia-iscanprofilemgr-openprofile.md)                             | Открывает профиль сканирования, сохраненный на диске в виде XML-файла.<br/>                                            |
| [**Обновить**](-wia-iscanprofilemgr-refresh.md)                                     | Повторно перечисляет все профили сканирования в системе.<br/>                                                          |
| [**SetDefault**](-wia-iscanprofilemgr-setdefault.md)                               | Задает указанный профиль сканирования в качестве профиля по умолчанию.<br/>                                                     |



 

## <a name="remarks"></a>Комментарии

Чтобы создать объект **исканпрофилемгр** , используйте метод [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) со следующими параметрами:

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

Если профиль сканирования сохранен с помощью метода [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) , он сохраняется как XML-файл в% UserProfile% \\ Application Data \\ \\ Center \\ усерсканпрофилес.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофилемгр. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
