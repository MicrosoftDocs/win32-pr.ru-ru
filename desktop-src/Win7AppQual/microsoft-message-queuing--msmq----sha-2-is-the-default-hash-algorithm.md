---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: Очередь сообщений Майкрософт (MSMQ) — SHA 2 является алгоритмом хэширования по умолчанию.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f0d2476133ca7939bc90effa3842c0b90482ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265892"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>Очередь сообщений Майкрософт (MSMQ) — SHA 2 является алгоритмом хэширования по умолчанию.

## <a name="affected-platforms"></a>Затронутые платформы

 **Клиенты** — Windows XP Windows Vista, Windows \| \| 7  
**Серверы** — windows Server 2003 windows \| Server 2008 \| Windows Server 2008 R2  










## <a name="feature-impact"></a>Воздействие на функции

 **Серьезность** — низкая  
**Частота** -низкая  





## <a name="description"></a>Описание

В Windows 7 MSMQ использует SHA-2 в качестве значения по умолчанию при подписывании исходящего сообщения. Кроме того, все входящие сообщения должны быть подписаны SHA-2. Вы можете включить поддержку более низкого алгоритма шифрования с помощью раздела реестра, доступного для администратора.

## <a name="manifestation-of-impact"></a>Влияние на манифесты

-   MSMQ в Windows 2003 или ниже не будет принимать подписанные сообщения, поступающие от MSMQ в Windows 7
-   MSMQ в Windows 7 не будет принимать подписанные сообщения, полученные из Windows 2008 или ниже

## <a name="mitigation"></a>Меры по снижению риска

Чтобы использовать более надежный алгоритм подписи, пользователям следует рассмотреть возможность обновления до Windows 7. Чтобы обеспечить простой обмен подписанными сообщениями между Windows 7 и любой операционной системой нижнего уровня, администратор должен добавить соответствующие исключения на компьютерах MSMQ.

 

 



