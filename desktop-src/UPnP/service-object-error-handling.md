---
title: Обработка ошибок объекта службы
description: При возникновении ошибки в объекте службы возвращаемое значение для вызова IDispatch Invoke должно быть представлено как \_ исключение E \_ , а указатель параметра пексцептинфо в структуру ексцептинфо в необходимо заполнить.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd39d08dc7ca5152ca412df1a6fb67d6df524f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134034"
---
# <a name="service-object-error-handling"></a>Обработка ошибок объекта службы

При возникновении ошибки в объекте службы возвращаемое значение для вызова [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) должно быть представлено как \_ исключение E \_ , а указатель параметра *пексцептинфо* на структуру [**ексцептинфо**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) в необходимо заполнить.

В частности, члены **бстрсаурце** и **bstrDescription** структуры [**ексцептинфо**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) используются узлом устройства с технологией UPnP для создания ответа на сбой UPnP. **бстрсаурце** — это код ошибки, а **bstrDescription** — описание ошибки.

 

 