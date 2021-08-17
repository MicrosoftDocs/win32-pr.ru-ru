---
description: Библиотека DbgHelp реализуется DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Версии DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5adb00c6442f7ba36f5aeb86e0255e175131492124d08fbf865e57a9721a7893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343864"
---
# <a name="dbghelp-versions"></a>Версии DbgHelp

Библиотека DbgHelp реализуется DbgHelp.dll. Несмотря на то, что эта библиотека DLL включена во все поддерживаемые версии Windows, она редко является самой актуальной версией DbgHelp. более того, версия DbgHelp, поставляемая в Windows, обладает ограниченной функциональностью других выпусков. в частности, в ней отсутствует поддержка сервера символов и исходного сервера.

последние версии DbgHelp.dll, SymSrv.dll и SrcSrv.dll доступны в составе [средств отладки для пакета Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) . Политики распространения для этих включенных библиотек DLL были специально разработаны для того, чтобы пользователи могли включать эти файлы в свои пакеты и выпуски.

> [!Caution]  
> пользователи никогда не должны пытаться установить [средства отладки для Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) версий DbgHelp.dll в системные каталоги Windows, так как они не проверяются в этом сценарии и, скорее всего, будут дестабилизировать систему. Существуют отдельные версии пакета отладки x64 и x86, и они необходимы для тех, кто заинтересован в поддержке обеих платформ.

Чтобы получить последнюю версию DbgHelp.dll, перейдите на страницу [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) и скачайте средства отладки для Windows. Сведения о правильной установке см. в разделе [вызов библиотеки DBGHELP](calling-the-dbghelp-library.md) .

> [!Note]  
> файл DbgHelp.dll, который поставляется в Windows, не является распространяемым.

Многие версии DbgHelp включают дополнительные функциональные возможности. Чтобы убедиться, что для приложения доступна правильная версия DbgHelp, ознакомьтесь со сведениями о требованиях в конкретной справочной документации по API.
