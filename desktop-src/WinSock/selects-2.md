---
description: В исходном интерфейсе сокета программного распространения Berkeley (BSD) функция Select была стандартной (и только) означает получение сетевых событий.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Бирает
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e50339f298c18c75ad6451590f191fc1bd8afba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702011"
---
# <a name="selects"></a>Бирает

В исходном интерфейсе сокета программного распространения Berkeley (BSD) функция [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) была стандартной (и только) означает получение сетевых событий. Для каждого сокета можно выполнить опрос или ожидание сведений о состоянии чтения, записи или ошибки. Дополнительные сведения см. в разделе [**вспселект**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) . Обратите внимание, что \_ этот подход не позволяет получить качество обслуживания с помощью фильтра событий сети.

 

 
