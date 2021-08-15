---
title: Функции обратного вызова yield
description: Функции обратного вызова yield
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Функции обратного вызова Авикап, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e87a3c986378bee05078b8cab28a0647827a1102ef1809558a47dcd5123af2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369138"
---
# <a name="yield-callback-functions"></a>Функции обратного вызова yield

Приложения могут использовать функцию yield callback во время потоковой записи. (Функция обратного вызова, как правило, состоит из цикла обработки сообщений, который вызывает [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)и [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage).) Окно Capture вызывает функцию обратного вызова yield по крайней мере один раз для каждого захваченного видеокадра, но Точная скорость зависит от частоты кадров и нагрузки на диск и драйвер записи.

 

 