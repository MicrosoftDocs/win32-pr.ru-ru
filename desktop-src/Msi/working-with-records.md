---
description: Установщик предоставляет функции, которые управляют записями в базе данных установки. Эти функции можно использовать совместно с функциями, описанными в разделе Работа с запросами для внесения фактических изменений в базу данных.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Работа с записями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f83159688ec106b8e3cea3021e4352c851620d0e2f89661cee823c1439c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498384"
---
# <a name="working-with-records"></a>Работа с записями

Установщик предоставляет функции, которые управляют записями в базе данных установки. Эти функции можно использовать совместно с функциями, описанными в разделе [Работа с запросами](working-with-queries.md) для внесения фактических изменений в базу данных.

Следующие функции создают или удаляют записи:

-   Чтобы создать новую запись для базы данных, вызовите функцию [**мсикреатерекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) .
-   Чтобы очистить данные из записи, присвойте каждому полю значение null, вызвав функцию [**мсирекордклеардата**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) .

Указанные поля записей заполняются следующими функциями:

-   Чтобы задать запись в целое число, вызовите функцию [**мсирекордсетинтежер**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) .
-   Чтобы задать запись в строку, вызовите функцию [**мсирекордсетстринг**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) .
-   Чтобы вставить весь файл в поле потока, вызовите функцию [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) .

Следующие функции считывают значения из указанных полей записей:

-   Чтобы считать целочисленное значение из поля, вызовите функцию [**мсирекорджетинтежер**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) .
-   Чтобы получить строковое значение, вызовите функцию [**мсирекорджетстринг**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) .
-   Чтобы получить поток, вызовите функцию [**мсирекордреадстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) .
-   Чтобы определить, имеет ли определенное поле записи значение null, вызовите функцию [**мсирекордиснулл**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) .

Следующие функции являются информационными функциями записи.

-   Чтобы получить число полей, содержащихся в записи, вызовите функцию [**мсирекорджетфиелдкаунт**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) .
-   Чтобы получить размер поля, вызовите функцию [**мсирекорддатасизе**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) . Возвращаемое значение **мсирекорддатасизе** чувствительно к типу поля.

 

 



