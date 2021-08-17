---
description: Пользователь может проверить состояние интерфейса Teredo из командной строки, введя команду netsh interface Teredo показывать состояние и проверив выходные данные.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: Одноранговая инфраструктура и Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18dfa3fe075d0829358849b3783272aac74e60545c1e58e1d9bf1663738e3721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794241"
---
# <a name="the-peer-infrastructure-and-teredo"></a>Одноранговая инфраструктура и Teredo

Пользователь может проверить состояние интерфейса [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) из командной строки, введя команду **netsh interface Teredo показывать состояние** и проверив выходные данные. Если состояние имеет значение "отключено", Teredo не активен, что запрещает пользователю подключаться к другим пользователям через адреса Teredo. Возможно, Teredo находится в автономном режиме, так как брандмауэр отключен или не поддерживает [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).

 

 
