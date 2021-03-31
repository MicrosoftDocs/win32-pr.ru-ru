---
description: Библиотека DbgHelp реализуется DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Версии DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811e92ba88bf38cb46274e2d2c716a620ea83b16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806958"
---
# <a name="dbghelp-versions"></a>Версии DbgHelp

Библиотека DbgHelp реализуется DbgHelp.dll. Хотя эта библиотека DLL включена во все поддерживаемые версии Windows, она редко является самой актуальной версией DbgHelp. Более того, версия DbgHelp, входящая в состав Windows, обладает ограниченной функциональностью других выпусков. в частности, она не поддерживает сервер символов и исходный сервер.

Новейшие версии DbgHelp.dll, SymSrv.dll и SrcSrv.dll доступны в составе пакета [средств отладки для Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) . Политики распространения для этих включенных библиотек DLL были специально разработаны для того, чтобы пользователи могли включать эти файлы в свои пакеты и выпуски.

> [!Caution]  
> Пользователи никогда не должны пытаться установить [средства отладки для версий windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) DbgHelp.dll в системные каталоги Windows, так как они не проверяются в этом сценарии и, скорее всего, будут дестабилизировать систему. Существуют отдельные версии пакета отладки x64 и x86, и они необходимы для тех, кто заинтересован в поддержке обеих платформ.

Чтобы получить последнюю версию DbgHelp.dll, перейдите на страницу [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) и скачайте средства отладки для Windows. Сведения о правильной установке см. в разделе [вызов библиотеки DBGHELP](calling-the-dbghelp-library.md) .

> [!Note]  
> Файл DbgHelp.dll, поставляемый в составе Windows, не является распространяемым.

Многие версии DbgHelp включают дополнительные функциональные возможности. Чтобы убедиться, что для приложения доступна правильная версия DbgHelp, ознакомьтесь со сведениями о требованиях в конкретной справочной документации по API.
