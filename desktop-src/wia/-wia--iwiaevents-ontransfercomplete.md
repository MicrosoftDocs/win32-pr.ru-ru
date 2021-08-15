---
description: Событие, возникающее при успешном завершении обмена данными.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Событие WIA. Онтрансферкомплете
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9095302a2f3fe75e1939ebb979ec4aad4d87b0462a5b40997e5523e7313d98e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209278"
---
# <a name="wiaontransfercomplete-event"></a>Событие WIA. Онтрансферкомплете

Событие, возникающее при успешном завершении обмена данными.

## <a name="syntax"></a>Синтаксис


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Элемент* 
</dt> <dd>

Объект [**Item**](-wia-item.md) передан.

</dd> <dt>

*Путь* 
</dt> <dd>

Путь и имя переданного образа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

WIA уведомляет сценарий или приложение об успешном завершении перемещения данных, изображения или звука. Реализуйте  \_ подпрограммы обжвиа **онтрансферкомплете ()** , чтобы сценарий или приложение отвечали на завершение передаваемых данных.

Например, может потребоваться, чтобы сценарий отображал изображение после его передачи.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




