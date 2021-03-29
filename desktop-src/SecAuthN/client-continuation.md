---
description: Для некоторых протоколов требуется несколько сообщений проверки подлинности.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Продолжение клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898638"
---
# <a name="client-continuation"></a>Продолжение клиента

Для некоторых протоколов требуется несколько сообщений проверки подлинности. В этом случае клиент анализирует ответ от сервера и вызывает [**InitializeSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) еще раз, используя состояние continue из предыдущего вызова. Клиент проверяет состояние возврата с помощью этого вызова и может потребоваться для продолжения дополнительных отрезков. Он использует сведения в *паутпут* для создания сообщения и его отправки на сервер.

 

 
