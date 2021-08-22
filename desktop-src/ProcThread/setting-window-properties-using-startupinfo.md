---
description: Родительский процесс может задавать свойства, связанные с главным окном его дочернего процесса.
ms.assetid: 12547da4-8d41-48c5-8efc-f0423f64caa7
title: Задание свойств окна с помощью СТАРТУПИНФО
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637e8fc9c76694a468b4b8fa6d5d2bd8a3432bbb7dad078d616df753244af358
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517384"
---
# <a name="setting-window-properties-using-startupinfo"></a>Задание свойств окна с помощью СТАРТУПИНФО

Родительский процесс может задавать свойства, связанные с главным окном его дочернего процесса. Функция [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) принимает указатель на структуру [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) в качестве одного из своих параметров. Члены этой структуры используются для указания характеристик главного окна дочернего процесса. Элемент **dwFlags** содержит битовое значение, определяющее, какие другие элементы структуры используются. Это позволяет указать значения для любого подмножества свойств окна. Система использует значения по умолчанию для свойств, которые не указаны. Элемент **dwFlags** также может принудительно отображать курсор обратной связи во время инициализации нового процесса.

Для процессов графического пользовательского интерфейса структура [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) указывает значения по умолчанию, которые будут использоваться при первом вызове новым процессом функций [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) и [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) для создания и вывода перекрывающихся окон. Можно указать следующие значения по умолчанию:

-   Ширина и высота окна, созданного с помощью [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), в пикселях.
-   Расположение в экранных координатах окна, созданного с помощью [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).
-   Параметр *нкмдшов* для [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).

Для процессов консоли используйте структуру [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) , чтобы указать свойства окна только при создании новой консоли (либо с помощью функции [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) с созданием \_ новой \_ консоли, либо с функцией [**аллокконсоле**](/windows/console/allocconsole) ). Структуру **стартупинфо** можно использовать для указания следующих свойств окна консоли:

-   Размер нового окна консоли в ячейках символов.
-   Расположение нового окна консоли в экранных координатах.
-   Размер (в ячейках символов) буфера экрана новой консоли.
-   Атрибуты текста и фона для буфера экрана новой консоли.
-   Заголовок окна новой консоли.

 

 
