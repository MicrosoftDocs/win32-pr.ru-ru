---
description: Пользователь может проверить состояние интерфейса Teredo из командной строки, введя команду netsh interface Teredo показывать состояние и проверив выходные данные.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: Одноранговая инфраструктура и Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2550d8da46339205de60c4a537d03c10940da4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545519"
---
# <a name="the-peer-infrastructure-and-teredo"></a>Одноранговая инфраструктура и Teredo

Пользователь может проверить состояние интерфейса [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) из командной строки, введя команду **netsh interface Teredo показывать состояние** и проверив выходные данные. Если состояние имеет значение "отключено", Teredo не активен, что запрещает пользователю подключаться к другим пользователям через адреса Teredo. Возможно, Teredo находится в автономном режиме, так как брандмауэр отключен или не поддерживает [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).

 

 
