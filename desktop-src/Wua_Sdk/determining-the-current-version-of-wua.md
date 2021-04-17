---
description: Определите версию агента Центр обновления Windows (WUA) перед его использованием.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Определение текущей версии WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701929"
---
# <a name="determining-the-current-version-of-wua"></a>Определение текущей версии WUA

Общие сведения об обновлении WUA, включая пошаговые инструкции по программному определению в приложении того, соответствует ли версия WUA, выполняемая на компьютере, требованиям, см. в разделе [обновление агента Центр обновления Windows](updating-the-windows-update-agent.md).

В версиях Windows, предшествующих Windows 7 и Windows Server 2008 R2, перед использованием необходимо определить установленную версию Центр обновления Windows Agent (WUA). Текущая версия WUA определяется версией Wuaueng.dll, которая выполняется в \\ подкаталоге system32 текущей установки Windows. Если версия Wuaueng.dll имеет версию 5.4.3790.1000 или более позднюю, то будет установлен WUA. Версия, более ранняя чем 5.4.3790.1000, указывает, что установлены службы Software Update Services (SUS) 1,0.

При обращении к службе SUS 1,0 с помощью API WUA возвращается **значение HRESULT** службы WU \_ E \_ Au \_ легацисервер.

Можно также использовать метод [**ивиндовсупдатеажентинфо::-info**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) для получения текущей версии файла Wuapi.dll, которая выполняется на компьютере. Интерфейс [**ивиндовсупдатеажентинфо**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) не поддерживается в WUA 1,0.
