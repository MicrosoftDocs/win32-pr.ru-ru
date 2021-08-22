---
title: Обработка ошибок объекта службы
description: При возникновении ошибки в объекте службы возвращаемое значение для вызова IDispatch Invoke должно быть представлено как \_ исключение E \_ , а указатель параметра пексцептинфо в структуру ексцептинфо в необходимо заполнить.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c98db4ffdb3c4625ec4c0dfbe3d497ab1cbe4b5152b172c34422c1630ce581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999524"
---
# <a name="service-object-error-handling"></a>Обработка ошибок объекта службы

При возникновении ошибки в объекте службы возвращаемое значение для вызова [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) должно быть представлено как \_ исключение E \_ , а указатель параметра *пексцептинфо* на структуру [**ексцептинфо**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) в необходимо заполнить.

В частности, члены **бстрсаурце** и **bstrDescription** структуры [**ексцептинфо**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) используются узлом устройства с технологией UPnP для создания ответа на сбой UPnP. **бстрсаурце** — это код ошибки, а **bstrDescription** — описание ошибки.

 

 