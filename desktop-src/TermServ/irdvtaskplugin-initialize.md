---
title: Метод инициализации Ирдвтаскплугин
description: Вызывается для инициализации агента задачи.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Инициализация метода службы удаленных рабочих столов
- Инициализация метода службы удаленных рабочих столов, интерфейс Ирдвтаскплугин
- Интерфейс Ирдвтаскплугин службы удаленных рабочих столов, метод Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14f4a002a0b33e403c02dba74385edd21e211fb27bcfb144c7a9ddc080a40fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606107"
---
# <a name="irdvtaskplugininitialize-method"></a>Метод Ирдвтаскплугин:: Initialize

Вызывается для инициализации агента задачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнотифисинк* \[ окне\]
</dt> <dd>

Тип: **[ **ирдвтаскплугиннотифисинк**](irdvtaskpluginnotifysink.md)\***

Указатель на интерфейс [**ирдвтаскплугиннотифисинк**](irdvtaskpluginnotifysink.md) , который агент задачи использует для взаимодействия с агентом триггера. Этот интерфейс необходимо освобождать, если он больше не нужен.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Windows 7 Корпоративная<br/>   |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ирдвтаскплугин**](irdvtaskplugin.md)
</dt> </dl>

 

 





