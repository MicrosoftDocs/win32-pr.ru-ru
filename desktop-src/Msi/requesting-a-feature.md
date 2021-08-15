---
description: Существует несколько функций, которые приложение должно вызвать для запроса функций.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Запрос функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288804168f6adf936550fee0ac0c542bd68f4d468d6aedd6372071744b9fec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990567"
---
# <a name="requesting-a-feature"></a>Запрос функции

Существует несколько функций, которые приложение должно вызвать для запроса функций. Перед запросом функции приложение должно убедиться, что эта функция установлена. Если приложение вызывает [**мсиусефеатуре**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) до того, как приложение обращается к функции, приложение может использовать полученные сведения для поддержки метрик использования.

**Запрос функции**

1.  Вызовите функцию [**мсиенумфеатурес**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) или [**мсикуерифеатурестате**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) , если требуется определить доступность компонента без увеличения числа использований.
2.  Укажите намерение приложения использовать функцию, вызвав функцию [**мсиусефеатуре**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .
3.  Определите расположение файлов, вызвав функцию [**мсижеткомпонентпас**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .
4.  Настройте компонент, вызвав функцию [**мсиконфигурефеатуре**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .
5.  Получите метрики использования, которые приложение может использовать, вызвав функцию [**мсижетфеатуреусаже**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .

На следующей схеме показана модель запросов функций.

![модель запроса функций. ](images/over2.png)

 

 



