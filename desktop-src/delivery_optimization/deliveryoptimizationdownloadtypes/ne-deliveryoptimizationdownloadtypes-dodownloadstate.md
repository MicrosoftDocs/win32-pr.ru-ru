---
title: Перечисление Додовнлоадстате
description: Указывает идентификатор текущего состояния загрузки, который является частью структуры **DO_DOWNLOAD_STATUS** .
keywords:
- Перечисление Додовнлоадстате, Додовнлоадстате
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534931"
---
# <a name="dodownloadstate-enumeration"></a>Перечисление Додовнлоадстате

Перечисление **додовнлоадстате** указывает идентификатор текущего состояния загрузки, который является частью структуры **DO_DOWNLOAD_STATUS** .

## <a name="syntax"></a>Синтаксис

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a>Константы

| Требование | Значение |
|-|-|
| DODownloadState_Created | Объект скачивания создан, но еще не запущен. |
| DODownloadState_Transferring | Идет скачивание. |
| DODownloadState_Transferred | Загрузка передается, и ее можно запустить снова, загрузив другую часть файла. |
| DODownloadState_Finalized | Скачивание завершено, и его невозможно запустить снова. |
| DODownloadState_Aborted | Скачивание прервано. |
| DODownloadState_Paused | Скачивание приостановлено по требованию или из-за временной ошибки. |

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Деливерйоптимизатиондовнлоадтипес. h |
