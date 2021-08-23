---
description: Сравните аргумент с активной конфигурацией сборщика.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Метод Исконфигуратионекуал класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 6facd4f885eb1eb992f95bf4432e32704f7472d8125cb1022f7a6baf5cf591d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579674"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a>Метод Исконфигуратионекуал класса Control

Сравните аргумент с активной конфигурацией сборщика.

## <a name="syntax"></a>Синтаксис


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Конфигурация* \[ окне\]
</dt> <dd>

Конфигурация, сравниваемая с активной конфигурацией.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

<dl> <dt>


</dt> <dd>

0

Сбой

</dd> <dt>


</dt> <dd>

1

Успешно

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                       |
| Пространство имен<br/>                | корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор<br/>                                              |
| MOF<br/>                      | <dl> <dt>Бутевентколлекторвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент**](control.md)
</dt> </dl>

 

 




