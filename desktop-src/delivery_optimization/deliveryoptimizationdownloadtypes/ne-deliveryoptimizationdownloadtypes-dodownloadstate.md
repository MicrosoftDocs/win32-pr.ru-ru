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
ms.openlocfilehash: 5df8f7b20c8cff3b905acec9852b26c9a5ee360645fddb1bec22990a8bb9daba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047142"
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

## <a name="requirements"></a>Requirements (Требования)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Деливерйоптимизатиондовнлоадтипес. h |
