---
description: Структура КОММКОНФИГ определяет конфигурацию ресурса связи, последовательного или иным образом.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Конфигурация ресурса связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01cd85a60eabc3cf6adcbdb0e05d2fbdc662442029044a5ac67d9a37bc073d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918324"
---
# <a name="communications-resource-configuration"></a>Конфигурация ресурса связи

Структура [**коммконфиг**](/windows/desktop/api/Winbase/ns-winbase-commconfig) определяет конфигурацию ресурса связи, последовательного или иным образом. Формат структуры зависит от типа ресурса связи (подтип поставщика). Первые несколько элементов структуры являются общими для всех коммуникационных ресурсов; дополнительные члены определяются для конкретных подтипов поставщика. Определенные поставщики услуг также могут расширить структуру **коммконфиг** .

Приложение может получить и настроить конфигурацию ресурса связи с помощью функций [**жеткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) и [**сеткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) . При открытии ресурс связи инициализируется с использованием конфигурации по умолчанию для подтипа поставщика. Чтобы получить и задать конфигурацию по умолчанию для подтипа поставщика, используйте функции [**жетдефаулткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) и [**сетдефаулткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .

Чтобы запросить у пользователя сведения о конфигурации, используйте функцию [**коммконфигдиалог**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) . Эта функция отображает диалоговое окно, определенное поставщиком услуг, и заполняет структуру [**коммконфиг**](/windows/desktop/api/Winbase/ns-winbase-commconfig) на основе введенных пользователем данных.

 

 



