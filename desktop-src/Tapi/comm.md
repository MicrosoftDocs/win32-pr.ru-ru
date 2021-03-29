---
description: Класс устройства взаимодействия состоит из портов связи. Доступ к этим устройствам осуществляется с помощью функций File и Communications.
ms.assetid: c1cf4998-b752-4cfd-9dd7-c9872b62c44b
title: портов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40136654d7e308f30e4e27467cf5e21385340841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810900"
---
# <a name="comm"></a>портов

Класс устройства взаимодействия состоит из портов связи. Доступ к этим устройствам осуществляется с помощью функций [File](/windows/desktop/FileIO/file-management-functions) и [Communications](/windows/desktop/DevIO/communications-functions).

Функция [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая для элемента **двстрингформат** \_ значение STRINGFORMAT ASCII и добавляя строку, завершающуюся нулем, которая указывает имя коммуникационного устройства (например, имя модема).

 

 
