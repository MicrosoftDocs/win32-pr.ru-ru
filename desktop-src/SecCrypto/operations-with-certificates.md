---
description: Интерфейс CryptoAPI предоставляет функции для работы с сертификатами, списками отзыва сертификатов (CRL) и списками доверия сертификатов (CTL).
ms.assetid: 23460329-44ed-4bcb-9727-5c841070f093
title: Операции с сертификатами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2f9f5d6d541b452741f2e4634752b979f26107
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912015"
---
# <a name="operations-with-certificates"></a>Операции с сертификатами

Интерфейс [*CryptoAPI*](../secgloss/c-gly.md) предоставляет функции для работы с [*сертификатами*](../secgloss/c-gly.md), [*списками отзыва сертификатов*](../secgloss/c-gly.md) (CRL) и [*списками доверия сертификатов*](../secgloss/c-gly.md) (CTL). К ним относятся функции для преобразования закодированных типов в типы контекста, функции, которые дублируют объекты и функции, освобождающие эти объекты. Эти функции кодируют информацию в контексты, но не добавляют этот контекст в любое хранилище. Эти функции — [**церткреатецертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), [**церткреатекрлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)и [**церткреатектлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext). Используйте соответствующую функцию Цертфри, чтобы освободить контексты, созданные одной из этих функций.

Функции CryptoAPI для дублирования сертификатов, списков отзыва сертификатов и CTL увеличивают [*счетчик ссылок*](../secgloss/r-gly.md) в указанном контексте и возвращают указатель на контекст. Функции дублирования не выделяют дополнительное пространство или не копируют данные из контекста в новое место в памяти. Эти функции — [**цертдупликатецертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext), [**цертдупликатекрлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)и [**цертдупликатектлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext). Контексты, созданные с помощью любой из этих функций, должны быть освобождены с помощью соответствующей функции Цертфри.

Функции CryptoAPI, которые освобождают сертификаты, списки отзыва сертификатов и списки CTL, являются [**цертфрицертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**цертфрикрлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)и [**цертфриктлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext). Каждая из этих функций уменьшает [*число ссылок*](../secgloss/r-gly.md) в контексте. Если счетчик ссылок достигает нуля, память, выделенная для контекста, освобождается.

Полные списки функций для работы с сертификатами, списками отзыва сертификатов и списками CTL см. в разделе [функции обслуживания сертификатов и хранилища сертификатов](cryptography-functions.md), функции [сертификатов](cryptography-functions.md), [функции списка отзыва сертификатов](cryptography-functions.md)и [функции списков доверия сертификатов](cryptography-functions.md).

 

 
