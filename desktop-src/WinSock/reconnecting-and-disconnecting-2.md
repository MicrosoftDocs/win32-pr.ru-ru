---
description: Назначение по умолчанию можно изменить, просто вызвав Вспконнект еще раз, даже если сокет уже подключен. Все датаграммы, поставленные в очередь на получение, отбрасываются, если новый адрес отличается от адреса, указанного в предыдущем Вспконнект.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Повторное подключение и отключение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898810"
---
# <a name="reconnecting-and-disconnecting"></a>Повторное подключение и отключение

Назначение по умолчанию можно изменить, просто вызвав [**вспконнект**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) еще раз, даже если сокет уже подключен. Все датаграммы, поставленные в очередь на получение, отбрасываются, если новый адрес отличается от адреса, указанного в предыдущем **вспконнект**.

Если адрес, указанный для сокета, равен нулю, сокет будет отключен — удаленный адрес по умолчанию будет неопределенным, поэтому вызовы [**вспсенд**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) и [**вспрекв**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) будут возвращать код ошибки всаенотконн, хотя [**вспсендто**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) и [**вспреквфром**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) по-прежнему могут использоваться.

 

 
