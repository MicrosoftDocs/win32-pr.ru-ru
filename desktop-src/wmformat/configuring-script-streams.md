---
title: Настройка потоков скриптов
description: Настройка потоков скриптов
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- потоки, Настройка потоков скриптов
- кодеки, Настройка потоков сценариев
- Создание скриптов для потоков, Настройка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067847"
---
# <a name="configuring-script-streams"></a>Настройка потоков скриптов

Как и для всех произвольных типов потоков, потоки сценариев должны иметь определенную скорость потока и окно буфера. Основной тип носителя в структуре [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) должен быть установлен в вммедиатипе \_ script.

Для потоков сценариев необходимо, чтобы член **форматтипе** **\_ \_ типа мультимедиа WM** был установлен в вмформат \_ скрипт, который указывает, что элемент **пбформат** указывает на структуру [**вмскриптформат**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .

Существует только один поддерживаемый тип скрипта, ВМСКРИПТТИПЕ \_ твострингс.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Общая конфигурация для всех потоков**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Настройка произвольных типов потоков**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Команды скриптов**](script-commands.md)
</dt> </dl>

 

 




