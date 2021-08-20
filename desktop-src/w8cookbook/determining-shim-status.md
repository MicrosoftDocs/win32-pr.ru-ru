---
title: Определение состояния оболочки совместимости
description: Определение состояния оболочки совместимости
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcac24017dc4bc4de1f9eddb1919cc8190ccf7d98cda2f127428f1d227ef1d42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117672062"
---
# <a name="determining-shim-status"></a>Определение состояния оболочки совместимости

## <a name="platforms"></a>Платформы

<dl> Клиенты — Windows 8  
Серверы — Windows Server 2012  
</dl>

## <a name="description"></a>Описание

Windows 8 регистрирует события, когда приложения оболочкой совместимости по различным причинам. Самый простой способ определить, является ли ваше приложение оболочкой совместимости, — проверить средство просмотра событий. последовательно выберите приложения и службы журналы \\ телеметрия Microsoft Windows Application-Experience программы \\ .

## <a name="mitigation"></a>Меры по снижению риска

Лучший способ выйти из оболочек совместимости небольшого — переименовать исполняемый файл или увеличить основной номер версии на 1 (перекомпилировать исполняемый файл).

 

 




