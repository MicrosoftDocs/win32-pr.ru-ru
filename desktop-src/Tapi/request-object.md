---
description: Объект запроса создается с помощью CoCreateInstance COM и предоставляет один интерфейс Итрекуест.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Объект запроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcf6da101c3642ffe31b05efb18279a79bcfc28ed24af7a959f3275d9cbc4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905894"
---
# <a name="request-object"></a>Объект запроса

Объект запроса создается с помощью **COCREATEINSTANCE** com и предоставляет один интерфейс [**итрекуест**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest). Этот интерфейс предоставляет метод [**MAKECALL**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , позволяющий приложению TAPI 3 использовать телефонные телефония. Служба поддержки телефонии предоставляет приложениям с поддержкой телефонии простой механизм для телефонных звонков, не требуя от разработчика полноценного участия в телефонии.

Например, приложение электронной таблицы может добавить кнопку "позвонить" с помощью вспомогательной телефонии, не реализуя более сложные элементы управления, доступные в полном приложении TAPI.

Дополнительные сведения см. в [обзоре службы технической поддержки](assisted-telephony-overview.md) .

 

 



