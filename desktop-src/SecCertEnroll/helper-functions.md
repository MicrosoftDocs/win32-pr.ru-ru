---
description: В каждом из следующих разделов обсуждается функция, экспортируемая с помощью Xenroll.dll. В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Вспомогательные функции (API регистрации сертификатов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347745"
---
# <a name="helper-functions-certificate-enrollment-api"></a>Вспомогательные функции (API регистрации сертификатов)

В каждом из следующих разделов обсуждается функция, экспортируемая с помощью Xenroll.dll. В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует.

## <a name="binaryblobtostring"></a>бинариблобтостринг

Функция [**бинариблобтостринг**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) в Xenroll.dll преобразует массив байтов в строку.

С помощью CertEnroll.dll можно вызвать метод [**вариантбитеаррайтостринг**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) в интерфейсе [**ибинариконвертер**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .

## <a name="stringtobinaryblob"></a>стрингтобинариблоб

Функция [**стрингтобинариблоб**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) в Xenroll.dll преобразует строку в массив байтов.

С помощью CertEnroll.dll можно вызвать метод [**стрингтовариантбитеаррай**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) в интерфейсе [**ибинариконвертер**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сопоставление Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ибинариконвертер**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
