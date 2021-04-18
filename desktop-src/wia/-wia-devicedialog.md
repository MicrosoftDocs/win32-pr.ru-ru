---
description: Используется приложениями для вывода пользователем диалогового окна устройства.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Функция Девицедиалог (Виадевд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693078"
---
# <a name="devicedialog-function"></a>Функция Девицедиалог

Используется приложениями для вывода пользователем диалогового окна устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевицедиалогдата* \[ окне\]
</dt> <dd>

Тип: **пдевицедиалогдата**

[**Девицедиалогдата**](-wia-devicedialogdata.md) , используемый для создания диалогового окна устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Виадевд. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**девицедиалогдата**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




