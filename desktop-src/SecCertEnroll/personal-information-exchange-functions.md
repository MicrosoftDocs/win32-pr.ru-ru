---
description: В каждом из следующих разделов описывается функция, экспортируемая Xenroll.dll для управления сообщениями обмена личной информацией (PFX).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Функции обмена личной информацией
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683950"
---
# <a name="personal-information-exchange-functions"></a>Функции обмена личной информацией

В каждом из следующих разделов описывается функция, экспортируемая Xenroll.dll для управления сообщениями обмена личной информацией (PFX). В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует.

## <a name="createfilepfxwstr"></a>креатефилепфксвстр

Функция [**креатефилепфксвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) в Xenroll.dll сохраняет цепочку сертификатов и [*закрытый ключ*](/windows/desktop/SecGloss/p-gly) в файле с помощью формата PFX.

Библиотека CertEnroll.dll напрямую не реализует функции для копирования PFX-сообщения в файл. Однако можно использовать метод [**креатепфкс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) в интерфейсе [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) для создания закодированного сообщения PFX и написать пользовательскую функцию для сохранения сообщения в файле.

## <a name="createpfxwstr"></a>креатепфксвстр

Функция [**креатепфксвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) в Xenroll.dll сохраняет цепочку сертификатов и закрытый ключ в строке формата PFX.

Для создания закодированного сообщения PFX, содержащего цепочку сертификатов и ключ, можно использовать метод [**креатепфкс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) в интерфейсе [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . Можно указать пароль, параметры экспорта и тип кодировки. Чтобы получить строку, эквивалентную возвращенной из [**креатепфксвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), передайте \_ \_ \_ двоичный флаг кскн шифрования String в в параметре *Encoding* метода [**креатепфкс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сопоставление Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
