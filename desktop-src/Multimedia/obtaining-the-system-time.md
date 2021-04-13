---
title: Получение системного времени
description: Получение системного времени
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- Таймеры мультимедиа, системное время
- таймеры, системное время
- системное время
- Функция Тимежеттиме
- Функция Тимежетсистемтиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487572"
---
# <a name="obtaining-the-system-time"></a>Получение системного времени

Как правило, прежде чем приложение начнет использовать службы таймера мультимедиа, оно получает текущее *системное время*. Системное время — это время в миллисекундах, с момента запуска операционной системы Microsoft Windows. Для получения системного времени можно использовать функцию [**тимежеттиме**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) или [**тимежетсистемтиме**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) . Эти две функции очень похожи: **тимежеттиме** возвращает системное время, а **Тимежетсистемтиме** заполняет структуру [**ммтиме**](/previous-versions//dd757347(v=vs.85)) с системным временем.

 

 