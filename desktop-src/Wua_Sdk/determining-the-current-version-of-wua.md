---
description: определите версию агента Центр обновления Windows (WUA) перед его использованием.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Определение текущей версии WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d8e013f4e8189c71b9e4510fdaebcdf1e2f749e3d8dfffd6256128e214ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049502"
---
# <a name="determining-the-current-version-of-wua"></a>Определение текущей версии WUA

общие сведения об обновлении wua, включая пошаговые инструкции по программному определению в приложении того, соответствует ли версия WUA, выполняемая на компьютере, требованиям, см. в разделе [обновление агента Центр обновления Windows](updating-the-windows-update-agent.md).

в версиях Windows до Windows 7 и Windows Server 2008 R2 перед использованием необходимо определить установленную версию Центр обновления Windows Agent (WUA). текущая версия WUA определяется версией Wuaueng.dll, которая выполняется в \\ подкаталоге System32 текущей установки Windows. Если версия Wuaueng.dll имеет версию 5.4.3790.1000 или более позднюю, то будет установлен WUA. Версия, более ранняя чем 5.4.3790.1000, указывает, что установлены службы Software Update Services (SUS) 1,0.

При обращении к службе SUS 1,0 с помощью API WUA возвращается **значение HRESULT** службы WU \_ E \_ Au \_ легацисервер.

Можно также использовать метод [**ивиндовсупдатеажентинфо::-info**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) для получения текущей версии файла Wuapi.dll, которая выполняется на компьютере. Интерфейс [**ивиндовсупдатеажентинфо**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) не поддерживается в WUA 1,0.
