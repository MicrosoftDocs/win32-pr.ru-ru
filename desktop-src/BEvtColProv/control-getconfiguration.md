---
description: Считывает активную конфигурацию сборщика.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Метод настройки класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: a877b4ae061b6568b877d9b8ee65b8d9b0380a012d7fdba28408ad4bfcae7030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579724"
---
# <a name="getconfiguration-method-of-the-control-class"></a>Метод настройки класса Control

Считывает активную конфигурацию сборщика.

## <a name="syntax"></a>Синтаксис


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тиместамплов* \[ заполняет\]
</dt> <dd>

При возврате из этого метода этот параметр содержит младшие биты метки времени, указывающие, когда была задана конфигурация.

</dd> <dt>

*Тиместамфигх* \[ заполняет\]
</dt> <dd>

При возврате из этого метода этот параметр содержит старшие биты метки времени, указывающие, когда была задана конфигурация.

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

 

 




