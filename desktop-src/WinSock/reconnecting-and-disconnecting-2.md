---
description: Назначение по умолчанию можно изменить, просто вызвав Вспконнект еще раз, даже если сокет уже подключен. Все датаграммы, поставленные в очередь на получение, отбрасываются, если новый адрес отличается от адреса, указанного в предыдущем Вспконнект.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Повторное подключение и отключение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4c50872b6690c42d97c3696bcfcb2586b9b5b510c17aafc5dcc159b17ed56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121364"
---
# <a name="reconnecting-and-disconnecting"></a>Повторное подключение и отключение

Назначение по умолчанию можно изменить, просто вызвав [**вспконнект**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) еще раз, даже если сокет уже подключен. Все датаграммы, поставленные в очередь на получение, отбрасываются, если новый адрес отличается от адреса, указанного в предыдущем **вспконнект**.

Если адрес, указанный для сокета, равен нулю, сокет будет отключен — удаленный адрес по умолчанию будет неопределенным, поэтому вызовы [**вспсенд**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) и [**вспрекв**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) будут возвращать код ошибки всаенотконн, хотя [**вспсендто**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) и [**вспреквфром**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) по-прежнему могут использоваться.

 

 
