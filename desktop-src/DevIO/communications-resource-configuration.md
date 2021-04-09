---
description: Структура КОММКОНФИГ определяет конфигурацию ресурса связи, последовательного или иным образом.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Конфигурация ресурса связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141519"
---
# <a name="communications-resource-configuration"></a>Конфигурация ресурса связи

Структура [**коммконфиг**](/windows/desktop/api/Winbase/ns-winbase-commconfig) определяет конфигурацию ресурса связи, последовательного или иным образом. Формат структуры зависит от типа ресурса связи (подтип поставщика). Первые несколько элементов структуры являются общими для всех коммуникационных ресурсов; дополнительные члены определяются для конкретных подтипов поставщика. Определенные поставщики услуг также могут расширить структуру **коммконфиг** .

Приложение может получить и настроить конфигурацию ресурса связи с помощью функций [**жеткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) и [**сеткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) . При открытии ресурс связи инициализируется с использованием конфигурации по умолчанию для подтипа поставщика. Чтобы получить и задать конфигурацию по умолчанию для подтипа поставщика, используйте функции [**жетдефаулткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) и [**сетдефаулткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .

Чтобы запросить у пользователя сведения о конфигурации, используйте функцию [**коммконфигдиалог**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) . Эта функция отображает диалоговое окно, определенное поставщиком услуг, и заполняет структуру [**коммконфиг**](/windows/desktop/api/Winbase/ns-winbase-commconfig) на основе введенных пользователем данных.

 

 



