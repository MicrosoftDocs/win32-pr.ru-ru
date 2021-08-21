---
title: Справочник по API службы удаленных рабочих столов Аудиоендпоинт
description: Поддерживает интерфейсы для регистрации конечных точек аудио и передачи данных.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Справочник по API Аудиоендпоинт службы удаленных рабочих столов службы удаленных рабочих столов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9a7aa83b519ca10128f9bea3b945492f387c0498c81f8b2959cb9830b91dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000094"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>Справочник по API службы удаленных рабочих столов Аудиоендпоинт

*Конечная точка аудио* представляет собой звуковое устройство, аудио API или любой другой источник или приемник звука, и используется для отправки данных в модуль аудио и получения данных из него. Конечная точка аудио должна быть подключена к подсистеме аудио с помощью *подключения*, и к каждому подключению может быть подключена только одна конечная точка. После регистрации конечной точки обработчик звука присоединяет конечную точку к подключению.

Каждый объект конечной точки должен реализовывать следующие интерфейсы:

-   [**Иаудиоендпоинт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) , чтобы включить обработчику аудио для получения сведений о конечной точке.
-   [**Иаудиоендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) получить сведения о буфере данных перед выполнением прохода обработки и уведомить конечную точку о завершении прохода.
-   Интерфейс [**иаудиоинпутендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) или [**иаудиуутпутендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) в зависимости от того, захватывается ли объект конечной точки или готовится к просмотру.
-   [**иаудиодевицеендпоинт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**иаудиоендпоинтконтрол**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

Обработчик аудио использует эти интерфейсы для получения сведений о конечных точках, подключенных к подсистеме. Реализация конечной точки должна предоставлять механизм для доставки данных в подсистему или получения данных из него, как указано в этих интерфейсах.

Службы удаленных рабочих столов API Аудиоендпоинт поддерживает типы перечисления, интерфейсы и структуры.

## <a name="in-this-section"></a>Содержание раздела

-   [Типы перечисления службы удаленных рабочих столов Аудиоендпоинт](terminal-services-audioendpoint-enumeration-types.md)
-   [службы удаленных рабочих столов функции Аудиоендпоинт](remote-desktop-services-audioendpoint-functions.md)
-   [Интерфейсы службы удаленных рабочих столов Аудиоендпоинт](terminal-services-audioendpoint-interfaces.md)
-   [службы удаленных рабочих столов структур Аудиоендпоинт](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>Remarks

Службы удаленных рабочих столов API Аудиоендпоинт для использования в сценариях удаленный рабочий стол; Он не предназначен для клиентских приложений.

 

 




