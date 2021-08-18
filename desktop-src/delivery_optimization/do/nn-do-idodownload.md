---
title: Интерфейс Идодовнлоад
description: Используется для запуска загрузки и управления им.
keywords:
- Интерфейс Идодовнлоад
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 356d6ae2e01f91eae94d9d2ff01a39dd49708eb73a7287d8c176b4231654a74a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543821"
---
# <a name="idodownload-interface"></a>Интерфейс Идодовнлоад

Интерфейс **идодовнлоад** используется для запуска загрузки и управления им.

## <a name="methods"></a>Методы

Интерфейс **идодовнлоад** содержит следующие методы.

| Метод | Описание |
| ---- |:---- |
| [Идодовнлоад:: Abort](./nf-do-idomanager-createdownload.md) | Прерывает скачивание. |
| [Идодовнлоад:: Finalize](./nf-do-idodownload-finalize.md) | Завершает скачивание. |
| [Идодовнлоад:: Property](./nf-do-idodownload-getproperty.md) | Извлекает указатель на **вариант** , содержащий определенное свойство загрузки. |
| [Идодовнлоад::/Status](./nf-do-idodownload-getstatus.md) | Получает указатель на структуру **DO_DOWNLOAD_STATUS** , отражающую текущее состояние загрузки. |
| [Идодовнлоад::P Аусе](./nf-do-idodownload-pause.md) | Приостанавливает скачивание. |
| [Идодовнлоад:: SetProperty](./nf-do-idodownload-setproperty.md) | Задает свойство загрузки. |
| [Идодовнлоад:: Start](./nf-do-idodownload-start.md) | Запускает или возобновляет загрузку. |

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |