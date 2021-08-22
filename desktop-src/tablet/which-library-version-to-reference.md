---
description: В этом разделе описываются различия между двоичными версиями библиотеки для планшетных ПК.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Версия библиотеки для ссылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899866dd11bbe72f9476ee3b645ed4e5612fe7043dae38675bd206e81562ca68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589284"
---
# <a name="which-library-version-to-reference"></a>Версия библиотеки для ссылки

В этом разделе описываются различия между двоичными версиями библиотеки для планшетных ПК.

## <a name="tablet-pc-library-versions"></a>Версии библиотеки для планшетных ПК

двоичные файлы библиотеки Tablet PC (Microsoft.Ink.dll) были обновлены в Windows Vista. эти двоичные файлы называются "версия 6,0" для совместного инЦиде с версией Windows, в которой они освобождаются.

последний выпуск двоичных файлов, совместимых с Windows XP, называется "версия 1,7".

Windows SDK можно установить на компьютерах Vista и XP, а Windows SDK включает обе версии Microsoft.Ink.dll.

Они устанавливаются в:

1. % ProgramFiles% \\ эталонных сборок \\ Microsoft \\ Tablet PC \\ v 1.7 \\Microsoft.Ink.dll

2. % ProgramFiles% \\ эталонных сборок \\ Microsoft \\ Tablet PC \\ v 6.0 \\Microsoft.Ink.dll

двоичные файлы версии 6,0 совместимы только с Windows Vista, и приложения, написанные на них, должны выполняться только в Windows Vista.

приложение, написанное для двоичных файлов версии 1,7, должно выполняться без изменений при установке в Windows Vista.

 

 



