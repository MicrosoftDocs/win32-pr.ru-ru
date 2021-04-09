---
title: Запись User-Initiated
description: Запись User-Initiated
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888860"
---
# <a name="user-initiated-capture"></a>Запись User-Initiated

Вы можете получить текущее значение флага записи, инициированного пользователем, с помощью сообщения [**о \_ \_ \_ \_ настройке получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Значение флага хранится в элементе **фмакеусерхитоктокаптуре** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) . Вы можете предоставить пользователю точный контроль над временем запуска сеанса записи, установив для этого члена **значение true**. Авикап отображает диалоговое окно после выделения всех буферов видео и аудио для сеанса записи. Это позволяет пользователю устранить задержки записи из-за инициализации программного обеспечения. Если приложение использует небольшое количество буферов видео, это диалоговое окно, вероятно, не требуется. Значение по умолчанию — **false**.

 

 




