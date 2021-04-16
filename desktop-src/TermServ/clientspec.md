---
title: Перечисление Клиентспек
description: Используется со свойством Клиентпротоколспек для указания протокола удаленного рабочего стола, используемого между клиентом и сервером.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов перечисления Клиентспек
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672520"
---
# <a name="clientspec-enumeration"></a>Перечисление Клиентспек

Используется со свойством [**клиентпротоколспек**](imsrdpclientadvancedsettings8-clientprotocolspec.md) для указания протокола удаленного рабочего стола, используемого между клиентом и сервером.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**фуллмоде**
</dt> <dd>

Это полный протокол удаленный рабочий стол Windows 8.

</dd> <dt>

<span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**синклиентмоде**
</dt> <dd>

Протокол ограничен использованием кодеков RemoteFX для Windows 7 с пакетом обновления 1 (SP1) и более компактного кэша. Все остальные кодеки отключены. Этот протокол имеет наименьший объем памяти.

</dd> <dt>

<span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**смаллкачемоде**
</dt> <dd>

Протокол аналогичен **фуллмоде**, за исключением того, что он использует меньший кэш.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings8:: Клиентпротоколспек**](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





