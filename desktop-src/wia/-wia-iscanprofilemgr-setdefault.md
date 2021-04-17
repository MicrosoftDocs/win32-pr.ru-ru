---
description: Задает указанный профиль сканирования в качестве профиля по умолчанию.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'Метод Исканпрофилемгр:: Сетдефаулт (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663395"
---
# <a name="iscanprofilemgrsetdefault-method"></a>Метод Исканпрофилемгр:: Сетдефаулт

Задает указанный профиль сканирования в качестве профиля по умолчанию.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псканпрофиле* \[ окне\]
</dt> <dd>

Тип: **[**исканпрофиле**](-wia-iscanprofile.md) \** _

Указатель на профиль.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Используйте метод **исканпрофилемгр:: сетдефаулт** , чтобы добавить `<Default>` элемент в профиль или удалить этот элемент из предыдущего профиля по умолчанию устройства.

Используйте метод [**сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) для изменения профиля по умолчанию.

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

 

 




