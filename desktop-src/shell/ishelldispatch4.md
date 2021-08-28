---
description: Расширяет объект IShellDispatch3.
title: Объект IShellDispatch4 (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: 057ef4082bac8d04c006d951db7d2d251be2f8c62e88af65bc1a69678514af81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969013"
---
# <a name="ishelldispatch4-object"></a>Объект IShellDispatch4

Расширяет объект [**IShellDispatch3**](ishelldispatch3.md) . В дополнение к свойствам и методам, поддерживаемым **IShellDispatch3**, **IShellDispatch4** поддерживает четыре дополнительных метода.

> [!Note]  
> **IShellDispatch4** реализован и доступен через объект [**Shell**](shell.md) .

 

## <a name="members"></a>Элементы

Объект **IShellDispatch4** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Объект **IShellDispatch4** содержит эти методы.



| Метод                                                     | Описание                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**експлорерполици**](ishelldispatch4-explorerpolicy.md)   | Возвращает значение для указанной политики Internet Explorer.<br/> |
| [**GetSetting**](ishelldispatch4-getsetting.md)           | Извлекает параметр глобальной оболочки.<br/>                        |
| [**тоггледесктоп**](ishelldispatch4-toggledesktop.md)     | Отображает или скрывает Рабочий стол.<br/>                           |
| [**виндовссекурити**](ishelldispatch4-windowssecurity.md) | отображает диалоговое окно **Безопасность Windows** .<br/>            |



 

## <a name="remarks"></a>Remarks

обсуждение Windows служб см. в документации по [службам](../services/services.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 6,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Объект оболочки**](shell.md)
</dt> <dt>

[**ишеллдиспатч**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> </dl>

 

 
