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
ms.openlocfilehash: de8a3d36472d51c24a2c007ad7be0be371a0b5d8bb39e75f457e204250e8f53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441682"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Виадевд. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**девицедиалогдата**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




