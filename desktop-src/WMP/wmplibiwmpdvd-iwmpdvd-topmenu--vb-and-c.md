---
title: ИВМПДВД Топмену, метод
description: Метод Топмену останавливает воспроизведение и отображает верхнее (или корневое) меню для текущего заголовка.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- Топмену метод Windows Media Player
- Топмену метод проигрывателя Windows Media Player, интерфейс ИВМПДВД
- Интерфейс ИВМПДВД Windows Media Player, метод Топмену
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718123"
---
# <a name="iwmpdvdtopmenu-method"></a>Метод ИВМПДВД:: Топмену

Метод **топмену** останавливает воспроизведение и отображает верхнее (или корневое) меню для текущего заголовка.

## <a name="syntax"></a>Синтаксис


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Каждый DVD-диск создан по-другому. Чтобы этот метод работал, DVD-диск должен содержать меню. Некоторые DVD-диски созданы таким образом, чтобы методы **топмену** и **ивмпдвд. титлемену** открывали одно и то же меню. Метод **топмену** обычно вызывает верхнее (или корневое) меню, но может вызвать меню заголовка, если нет доступного корневого меню.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс ИВМПДВД (VB и C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**ИВМПДВД. Титлемену (VB и C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





