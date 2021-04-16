---
description: Вспконнект устанавливает адрес назначения по умолчанию, чтобы разрешить использование сокета с последующими операциями Send (Вспсенд) и Receive (Вспрекв).
ms.assetid: efd57cb1-9736-4527-8e20-ab9304e3a8f6
title: Соединение с одноранговым узлом по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22ca4aff0cdc8560459dd2571d79a71a85fcc71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692297"
---
# <a name="connecting-to-a-default-peer"></a>Соединение с одноранговым узлом по умолчанию

Для сокета, привязанного к протоколу без подключения, операция, выполняемая [**вспконнект**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , просто устанавливает адрес назначения по умолчанию, чтобы сокет можно было использовать с последующими операциями отправки и получения, ориентированными на соединение ([**вспсенд**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) и [**вспрекв**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))). Все датаграммы, полученные с адреса, отличного от указанного адреса назначения, будут удалены.

 

 
