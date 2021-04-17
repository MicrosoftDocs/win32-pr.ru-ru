---
description: Установщик Windows могут устанавливать, удалять и обновлять сборки и сборки Win32, используемые средой CLR платформы Microsoft .NET.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662947"
---
# <a name="assemblies"></a>Сборки

Установщик Windows могут устанавливать, удалять и обновлять сборки и сборки Win32, используемые средой CLR платформы Microsoft .NET. Сборка обрабатывается установщик Windows как один компонент установщика. Все файлы, составляющие сборку, должны содержаться в одном компоненте установщика, указанном в таблице [Component](component-table.md) .

Установщик Windows, выполняющиеся в Windows Vista и Windows XP, могут устанавливать параллельные сборки. Параллельные сборки могут безопасно обмениваться сборками между несколькими приложениями и могут отменять негативные последствия совместного использования сборок, такие как конфликты DLL. Вместо единственной версии сборки, которая предполагает обратную совместимость со всеми приложениями, параллельное совместное использование сборок позволяет нескольким версиям сборки COM или Win32 выполняться одновременно в системе. Эта улучшенная возможность изолировать приложения является важной частью Microsoft .NET Framework. Дополнительные сведения см. в разделе [изолированные приложения и параллельные сборки](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

В следующих разделах описывается использование сборок с установщик Windows.

-   [Добавление сборок в пакет](adding-assemblies-to-a-package.md)
-   [Установка и удаление сборок](installing-and-removing-assemblies.md)
-   [Обновление сборок](updating-assemblies.md)
-   [Режимы переустановки сборок среды CLR](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Разделы реестра сборки, записанные установщик Windows](assembly-registry-keys-written-by-windows-installer-.md)

Сведения об установке приложений COM и COM+ 1,0 см. в статьях [Установка приложения COM+ с установщик Windows](installing-a-com--application-with-the-windows-installer.md), [Установка компонента COM в частном расположении](installing-a-com-component-to-a-private-location.md)и [Создание компонента COM в существующем пакете](make-a-com-component-in-an-existing-package-private.md).

 

 
