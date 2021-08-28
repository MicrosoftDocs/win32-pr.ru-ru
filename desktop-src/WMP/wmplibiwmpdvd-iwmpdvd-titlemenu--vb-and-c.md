---
title: ИВМПДВД Титлемену, метод
description: Метод Титлемену останавливает воспроизведение и отображает меню заголовка.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- проигрыватель Windows Media метода титлемену
- проигрыватель Windows Media метода титлемену, интерфейс ивмпдвд
- проигрыватель Windows Media интерфейса ивмпдвд, метод титлемену
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff485cd09915ec9acb076d2c06a8aa28c3549bf6527495e5e32d4a01d483285a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000464"
---
# <a name="iwmpdvdtitlemenu-method"></a>Метод ИВМПДВД:: Титлемену

Метод **титлемену** останавливает воспроизведение и отображает меню заголовка.

## <a name="syntax"></a>Синтаксис


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Каждый DVD-диск создан по-другому. Чтобы этот метод работал, DVD-диск должен содержать меню. Некоторые DVD-диски созданы таким образом, чтобы методы **ивмпдвд. топмену** и **титлемену** открывали одно и то же меню. Метод **титлемену** обычно вызывает меню заголовка, но он может вызвать верхнее меню, если нет доступного меню заголовка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс ИВМПДВД (VB и C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**ИВМПДВД. Топмену (VB и C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





