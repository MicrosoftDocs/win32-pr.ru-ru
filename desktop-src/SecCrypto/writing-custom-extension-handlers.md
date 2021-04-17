---
description: Чтобы создать пользовательские модули или закодировать сложное расширение, можно написать собственные обработчики расширений, которые экспортируют пользовательские интерфейсы.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Написание пользовательских обработчиков расширений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684157"
---
# <a name="writing-custom-extension-handlers"></a>Написание пользовательских обработчиков расширений

Чтобы создать пользовательские модули или закодировать сложное расширение, можно написать собственные обработчики расширений, которые экспортируют пользовательские интерфейсы. Службы сертификации Майкрософт поставляются со следующими интерфейсами, которые можно использовать для кодирования различных типов данных расширения: [**ицертенкодеалтнаме**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ицертенкодебитстринг**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ицертенкодекрлдистинфо**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ицертенкодедатеаррай**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)и [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray). Эти интерфейсы содержатся в Certenc.dll. Кроме того, сведения о типе для этих интерфейсов содержатся в Certencl.dll, который содержится в пакете SDK для платформы.

Дополнительные сведения о обработчиках расширений см. в разделе [обработчики расширений](extension-handlers.md).

 

 



