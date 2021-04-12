---
title: Определение состояния оболочки совместимости
description: Определение состояния оболочки совместимости
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331728"
---
# <a name="determining-shim-status"></a>Определение состояния оболочки совместимости

## <a name="platforms"></a>Платформы

<dl> Клиенты — Windows 8  
Серверы — Windows Server 2012  
</dl>

## <a name="description"></a>Описание

Windows 8 регистрирует события, когда приложения оболочкой совместимости по различным причинам. Самый простой способ определить, является ли ваше приложение оболочкой совместимости, — проверить средство просмотра событий. Последовательно выберите приложения и службы журналы \\ телеметрии Microsoft Windows Application-Experience Program \\ .

## <a name="mitigation"></a>Меры по снижению риска

Лучший способ выйти из оболочек совместимости небольшого — переименовать исполняемый файл или увеличить основной номер версии на 1 (перекомпилировать исполняемый файл).

 

 




