---
title: Структура MPSCAN_DATA (Мпклиент. h)
description: Просмотр данных, передаваемых в обратный вызов.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA структуры устаревшие функции среды Windows
- функции PMPSCAN_DATA Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b7c00357b8f104fff42b94de552d52979c364dee64a82bb8e438946319c8c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975994"
---
# <a name="mpscan_data-structure"></a>\_Структура данных мпскан

Просмотр данных, передаваемых в обратный вызов.

Эта структура содержит общую статистику угроз и ресурсов. Эти поля stat всегда являются допустимыми.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**ScanType**
</dt> <dd>

Тип: **[ **мпскан \_ тип**](mpscan-type.md)**

</dd> <dd>

Тип проверки.

</dd> <dt>

**ресаурцеинфо**
</dt> <dd>

Тип: **пмпресаурце \_ info** .

</dd> <dd>

Информация о ресурсе. См [**. \_ сведения о мпресаурце**](mpresource-info.md).

</dd> <dt>

**ресаурцестатс**
</dt> <dd>

Тип: **[ **мпресаурце \_ stats**](mpresource-stats.md)**

</dd> <dd>

Накопительная статистика, связанная с ресурсами.

</dd> <dt>

**среатстатс**
</dt> <dd>

Тип: **[ **мпсреат \_ stats**](mpthreat-stats.md)**

</dd> <dd>

Статистика угроз с успешным завершением сканирования.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_сведения о мпресаурце**](mpresource-info.md)
</dt> <dt>

[**\_Статистика мпресаурце**](mpresource-stats.md)
</dt> <dt>

[**\_тип мпскан**](mpscan-type.md)
</dt> <dt>

[**\_Статистика мпсреат**](mpthreat-stats.md)
</dt> </dl>

 

 





