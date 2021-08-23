---
description: Параллельные сборки можно устанавливать как общие сборки или как закрытые сборки. Дополнительные сведения см. в разделе Установка параллельных сборок в качестве частных сборок и установка параллельных сборок в качестве общих сборок.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Установка параллельных сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2124b490d64427e80b5beee53d1221cba4d5e59a23dc2d72c2da6833e14a98cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142137"
---
# <a name="installing-side-by-side-assemblies"></a>Установка параллельных сборок

Параллельные сборки можно устанавливать как [Общие сборки](/windows/desktop/Msi/shared-assemblies) или как [закрытые сборки](/windows/desktop/Msi/private-assemblies). Дополнительные сведения см. в разделе [Установка параллельных сборок в качестве частных сборок](installing-side-by-side-assemblies-as-private-assemblies.md) и [Установка параллельных сборок в качестве общих сборок](installing-side-by-side-assemblies-as-shared-assemblies.md).

Обратите внимание на следующее.

-   сборки, установленные в глобальный кэш сборок установкой с использованием [контекста установки](/windows/desktop/Msi/installation-context) "на пользователя", не защищаются с помощью Windows защиты файлов.
-   сборки, которые устанавливаются в глобальный кэш сборок установкой с использованием [контекста установки](/windows/desktop/Msi/installation-context) для компьютера, защищаются с помощью Windows защиты файлов.

 

 
