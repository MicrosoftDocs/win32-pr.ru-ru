---
description: Объект запроса создается с помощью CoCreateInstance COM и предоставляет один интерфейс Итрекуест.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Объект запроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673705"
---
# <a name="request-object"></a>Объект запроса

Объект запроса создается с помощью **COCREATEINSTANCE** com и предоставляет один интерфейс [**итрекуест**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest). Этот интерфейс предоставляет метод [**MAKECALL**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , позволяющий приложению TAPI 3 использовать телефонные телефония. Служба поддержки телефонии предоставляет приложениям с поддержкой телефонии простой механизм для телефонных звонков, не требуя от разработчика полноценного участия в телефонии.

Например, приложение электронной таблицы может добавить кнопку "позвонить" с помощью вспомогательной телефонии, не реализуя более сложные элементы управления, доступные в полном приложении TAPI.

Дополнительные сведения см. в [обзоре службы технической поддержки](assisted-telephony-overview.md) .

 

 



