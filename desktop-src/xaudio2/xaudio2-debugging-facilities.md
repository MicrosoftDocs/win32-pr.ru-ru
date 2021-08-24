---
description: Отладочная версия подсистемы XAudio2 проверяет параметры и предоставляет подробные сообщения о предупреждениях и ошибках.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Средства отладки XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc6a89bb298a2e836e4d8dc63ed0144b9a789950432c5c83f33ec7ad86f4de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706994"
---
# <a name="xaudio2-debugging-facilities"></a>Средства отладки XAudio2

Отладочная версия подсистемы XAudio2 проверяет параметры и предоставляет подробные сообщения о предупреждениях и ошибках.

## <a name="setting-the-debug-logging-level-at-run-time"></a>Настройка уровня ведения журнала отладки во время выполнения

Уровень отладочной информации, отображаемой XAudio2, можно задать в любое время, заполнив структуру [**\_ \_ конфигурации отладки XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) с флагами для требуемого уровня ведения журнала, а затем передать структуру методу [**IXAudio2:: сетдебугконфигуратион**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) . значения, передаваемые методу **IXAudio2:: сетдебугконфигуратион** , всегда переопределяют все значения по умолчанию, заданные в реестре Windows.

## <a name="debug-support"></a>Поддержка отладки

Средства отладки всегда доступны для XAUDIO2 в Windows 8.

В версиях XAUDIO2 для DirectX SDK необходимо использовать **\_ \_ модуль отладки XAUDIO2** при создании объекта XAUDIO2 с [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) , а для поддержки отладки в системе должна быть установлена среда выполнения разработчика DirectX SDK.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отладочные средства](debugging-facilities.md)
</dt> <dt>

[Справочник по программированию в XAudio2](programming-reference.md)
</dt> </dl>

 

 
