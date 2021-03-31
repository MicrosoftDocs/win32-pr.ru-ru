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
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337644"
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
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |