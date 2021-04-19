---
description: Указывает тип действия для операции защиты от потери данных конечной точки (DLP).
title: Перечисление Длпактионтипе (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495954"
---
# <a name="dlpactiontype-enumeration"></a>Перечисление Длпактионтипе

Указывает тип действия для операции защиты от потери данных конечной точки (DLP).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a>Константы

<dl> <dt>

*длпактионтипекопиторемоваблемедиа*
</dt> <dd>

Операция копирования на съемный носитель.

</dd> </dl>

<dl> <dt>

*длпактионтипекопитонетворкшаре*
</dt> <dd>

Операция копирования в общую сетевую папку.

</dd> </dl>

<dl> <dt>

*длпактионтипекопитоклипбоард*
</dt> <dd>

Операция копирования в буфер обмена.

</dd> </dl>

<dl> <dt>

*длпактионтипепринт*
</dt> <dd>

Операция печати.

</dd> </dl>


<dl> <dt>

*длпактионтипескринклип*
</dt> <dd>

Операция снимка экрана.

</dd> </dl>

<dl> <dt>

*длпактионтипеакцессбюналловедапп*
</dt> <dd>

Операция, выполняемая неразрешенным приложением.

</dd> </dl>


<dl> <dt>

*длпактионтипеклаудаппегресс*
</dt> <dd>

Операция, нацеленная на облачное расположение.

</dd> </dl>

<dl> <dt>

*длпактионтипеакцессбиблуетусапп*
</dt> <dd>

Операция, включающая доступ приложения Bluetooth.

</dd> </dl>

<dl> <dt>

*длпактионтипеакцессбирдпапп*
</dt> <dd>

Операция, которая включает доступ к удаленному рабочему столу.

</dd> </dl>

<dl> <dt>

*длпактионтипекаунт*
</dt> <dd>

Максимальное значение перечисления.

</dd> </dl>
 

## <a name="remarks"></a>Remarks

Значения из этого перечисления используются структурой [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .

## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |

