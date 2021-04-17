---
description: Метод Онлинедевице является устаревшим вместо более общего метода RequestStateChange, который непосредственно пересекается с функциями, предоставляемыми этим методом.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Метод Онлинедевице класса CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684283"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a>Метод Онлинедевице \_ класса CIM

Метод **онлинедевице** является устаревшим вместо более общего метода **RequestStateChange** , который непосредственно пересекается с функциями, предоставляемыми этим методом.

## <a name="syntax"></a>Синтаксис


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

В *сети* \[ окне\]
</dt> <dd>

Если **значение — true**, переведите устройство в режим «в сети», если **значение false**, перевести устройство в автономный режим.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Модель \_ CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




