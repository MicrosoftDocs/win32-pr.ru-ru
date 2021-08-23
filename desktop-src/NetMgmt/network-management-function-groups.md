---
title: Группы функций управления сетью
description: Функции управления сетью можно разделить на следующие группы.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e49a8c45c59031a12653f5cb863fef320a33c93bc60cabdd4cd6fb4aece9dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012512"
---
# <a name="network-management-function-groups"></a>Группы функций управления сетью

Функции управления сетью можно разделить на следующие группы:

-   [Функции предупреждений](alert-functions.md)
-   [Функции Апибуффер](apibuffer-functions.md)
-   [Функции службы каталогов](directory-service-functions.md)
-   [Функции распределенная файловая система (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [Получение функций](get-functions.md)
-   [Групповые функции](group-functions.md)
-   [Функции локальной группы](local-group-functions.md)
-   [Функции сообщений](message-functions.md)
-   [Функции Нетфиле](netfile-functions.md)
-   [Удаленные служебные функции](remote-utility-functions.md)
-   [Функции планирования](schedule-functions.md)
-   [Функции сервера](server-functions.md)
-   [Транспортные функции сервера и рабочей станции](server-and-workstation-transport-functions.md)
-   [Функции сеанса](session-functions.md)
-   [Функции общего доступа](share-functions.md)
-   [Статистические функции](/windows/desktop/NetShare/statistics-functions)
-   [Использование функций](use-functions.md)
-   [Пользовательские функции](user-functions.md)
-   [Пользовательские модальные функции](user-modal-functions.md)
-   [Пользовательские функции рабочих станций и рабочих станций](workstation-and-workstation-user-functions.md)

При программировании для Active Directory вы можете вызывать определенные методы интерфейса ADSI для достижения тех же функций, которые можно достичь, вызывая определенные функции управления сетью. Дополнительные сведения см. в разделе [сопоставление интерфейсов ADSI с функциями управления сетью](mapping-adsi-interfaces-to-the-network-management-functions.md).

Система также предоставляет независимый от сети набор сетевых функций ([внет функций](/windows/desktop/WNet/wnet-functions)), которые позволяют сетевым функциям работать с различными продуктами сетевых поставщиков. Если приложение можно преобразовать для использования функции Внет, необходимо выполнить преобразование. Существуют причины для внесения изменений:

-   Функции Внет являются независимыми от сети, а функции управления сетью работают только в сетях Майкрософт.
-   Некоторые функции могут не поддерживаться в будущих выпусках операционных систем Майкрософт, если они были заменены. Корпорация Майкрософт не планирует удалять определенные функции, пока не будет доступна эквивалентная или более высокая функциональность.

 

 