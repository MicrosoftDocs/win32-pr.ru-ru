---
description: Существует несколько функций, которые приложение должно вызвать для запроса функций.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Запрос функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081024"
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

 

 



