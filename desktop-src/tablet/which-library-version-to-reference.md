---
description: В этом разделе описываются различия между двоичными версиями библиотеки для планшетных ПК.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Версия библиотеки для ссылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692238"
---
# <a name="which-library-version-to-reference"></a>Версия библиотеки для ссылки

В этом разделе описываются различия между двоичными версиями библиотеки для планшетных ПК.

## <a name="tablet-pc-library-versions"></a>Версии библиотеки для планшетных ПК

Двоичные файлы библиотеки Tablet PC (Microsoft.Ink.dll) были обновлены в Windows Vista. Эти двоичные файлы называются "версия 6,0" для совместного инЦиде с версией Windows, в которой они освобождаются.

Последний выпуск двоичных файлов, совместимых с Windows XP, называется "версия 1,7".

Windows SDK можно установить на компьютерах Vista и XP, а Windows SDK включает обе версии Microsoft.Ink.dll.

Они устанавливаются в:

1. % ProgramFiles% \\ эталонных сборок \\ Microsoft \\ Tablet PC \\ v 1.7 \\Microsoft.Ink.dll

2. % ProgramFiles% \\ эталонных сборок \\ Microsoft \\ Tablet PC \\ v 6.0 \\Microsoft.Ink.dll

Двоичные файлы версии 6,0 совместимы только с Windows Vista, и приложения, написанные на них, должны выполняться только в Windows Vista.

Приложение, написанное для двоичных файлов версии 1,7, должно выполняться без изменений при установке в Windows Vista.

 

 



