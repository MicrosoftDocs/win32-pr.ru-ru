---
description: Windows установщик может устанавливать, удалять и обновлять сборки и сборки Win32, используемые средой clr Microsoft платформа .NET Framework.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a228dfad8155b9282f7ed5ee5c288a858f55c74c432ec6d21fd98aae58f98472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639276"
---
# <a name="assemblies"></a>Сборки

Windows установщик может устанавливать, удалять и обновлять сборки и сборки Win32, используемые средой clr Microsoft платформа .NET Framework. сборка обрабатывается установщик Windows как один компонент установщика. Все файлы, составляющие сборку, должны содержаться в одном компоненте установщика, указанном в таблице [Component](component-table.md) .

Windows установщик, работающий в Windows Vista и Windows XP, может устанавливать параллельные сборки. Параллельные сборки могут безопасно обмениваться сборками между несколькими приложениями и могут отменять негативные последствия совместного использования сборок, такие как конфликты DLL. Вместо единственной версии сборки, которая предполагает обратную совместимость со всеми приложениями, параллельное совместное использование сборок позволяет нескольким версиям сборки COM или Win32 выполняться одновременно в системе. эта улучшенная возможность изолировать приложения является важной частью платформа .NET Framework майкрософт. Дополнительные сведения см. в разделе [изолированные приложения и параллельные сборки](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

в следующих разделах описывается использование сборок с установщик Windows.

-   [Добавление сборок в пакет](adding-assemblies-to-a-package.md)
-   [Установка и удаление сборок](installing-and-removing-assemblies.md)
-   [Обновление сборок](updating-assemblies.md)
-   [Режимы переустановки сборок среды CLR](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [разделы реестра сборки, записанные установщик Windows](assembly-registry-keys-written-by-windows-installer-.md)

сведения об установке приложений com и COM+ 1,0 см. в статьях [установка приложения com+ с установщик Windows](installing-a-com--application-with-the-windows-installer.md), [установка компонента com в частном расположении](installing-a-com-component-to-a-private-location.md)и [создание компонента com в существующем пакете](make-a-com-component-in-an-existing-package-private.md).

 

 
