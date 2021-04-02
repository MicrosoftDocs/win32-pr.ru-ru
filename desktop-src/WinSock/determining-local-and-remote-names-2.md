---
description: Вспжетсоккнаме используется для получения локального адреса для привязанных сокетов.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Определение локальных и удаленных имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072748"
---
# <a name="determining-local-and-remote-names"></a>Определение локальных и удаленных имен

[**Вспжетсоккнаме**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) используется для получения локального адреса для привязанных сокетов. Это особенно полезно при вызове [**вспконнект**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) без предварительного выполнения [**вспбинд**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) . **Вспжетсоккнаме** предоставляет единственные средства для определения локальной связи, которая неявно задана поставщиком.

После настройки подключения можно использовать [**вспжетпирнаме**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) для определения адреса однорангового узла, к которому подключен сокет.

 

 
