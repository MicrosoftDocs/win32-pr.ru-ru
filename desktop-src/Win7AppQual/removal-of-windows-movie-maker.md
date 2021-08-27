---
description: удаление Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: удаление Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538032d589439ccc0966bc151568813eed3d1946cd2cb8ea7d9314246edb19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098524"
---
# <a name="removal-of-windows-movie-maker"></a>удаление Windows Movie Maker

## <a name="affected-platforms"></a>Затронутые платформы

**клиенты** — Windows 7  
**серверы** — Windows Server 2008 R2  









## <a name="feature-impact"></a>Воздействие на функции

 **Серьезность** — высокая  
**Частота** — средний  


## <a name="description"></a>Описание

корпорация майкрософт не является рекомендуемой и удаляет программу Windows Movie Maker. В том числе:

-   все точки входа в Windows Movie Maker (например, меню "пуск", запуск > запуск)
-   все двоичные файлы, которые использовались Windows Movie maker (все, что было в% ProgramFiles% \\ Movie maker)

Однако файлы проекта студии фильма пользователя останутся в системе и будут доступны другим приложениям, поддерживающим этот формат файлов.

## <a name="manifestation"></a>Проявление

удаление Windows Movie Maker приводит к следующим результатам:

-   любая попытка запустить Windows Movie Maker со своими аргументами командной строки завершится ошибкой
-   Все подключаемые модули, которые были установлены для включения новых преобразований и анимации, останутся установленными, но не будут доступны конечному пользователю.

## <a name="solution"></a>Решение

Чтобы иметь такие функциональные возможности в будущем, пользователю потребуется установить аналогичное приложение от корпорации Майкрософт или другого поставщика программного обеспечения.

 

 



