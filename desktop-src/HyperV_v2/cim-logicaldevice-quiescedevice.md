---
description: Метод Куиесцедевице является устаревшим вместо более общего метода RequestStateChange, который непосредственно пересекается с функциями, предоставляемыми этим методом.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Метод Куиесцедевице класса CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7becb86f19c245488d779e1b26ab5321ba3f2aa0ac3c7811d96f9d1cb8a5dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995696"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a>Метод Куиесцедевице \_ класса CIM

Метод **куиесцедевице** является устаревшим вместо более общего метода **RequestStateChange** , который непосредственно пересекается с функциями, предоставляемыми этим методом.

## <a name="syntax"></a>Синтаксис


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Замораживание* \[ окне\]
</dt> <dd>

Если задано значение **true** , то все действия, выполняемые в случае **ложной** операции возобновления, прекращают работу.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Модель \_ CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




