---
title: Библиотеки типов расширений ADSI
description: Библиотеки типов для расширений не объединяются.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- Библиотеки типов расширений ADSI ADSI
- расширения ADSI, библиотеки типов расширений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2390f587d5ce0d18e6e96aaf993115bb523feb340bf2becf60ceb2cff81d952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180834"
---
# <a name="adsi-extension-type-libraries"></a>Библиотеки типов расширений ADSI

Библиотеки типов для расширений не объединяются. Клиенты ADSI должны явно включать библиотеку типов для каждого расширения. библиотека типов необходима для Visual Basic для включения ранних привязок. Клиентские приложения, написанные на C/C++, могут вызывать метод **QueryInterface** для интерфейсов расширения, определенных в файлах заголовков расширений.

 

 




