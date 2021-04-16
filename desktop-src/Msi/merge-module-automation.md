---
description: Mergemod.dll предоставляет COM-объект, который реализует операции слияния и создание образов источника для модулей слияния. Основной объект реализует интерфейсы для программ C/C++ и клиентов автоматизации, включая Visual Basic и VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Автоматизация модуля слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651173"
---
# <a name="merge-module-automation"></a>Автоматизация модуля слияния

Mergemod.dll предоставляет COM-объект, который реализует операции слияния и создание образов источника для модулей слияния. Основной объект реализует интерфейсы для программ C/C++ и клиентов автоматизации, включая Visual Basic и VBScript.

Предпочтительный метод установки Mergemod.dll — с помощью установщик Windows. Идентификатор компонента для компонента, содержащего COM-интерфейс Mergemod.dll, — {FD153241-37EC-11D2-8892-00A0C981B015}. Один и тот же двоичный файл можно использовать во всех системах Windows, и библиотека DLL будет самостоятельно регистрироваться с помощью программы regsvr32 в старых системах.

Обратите внимание, что Mergemod.dll требует, чтобы Msvcrt.dll была установлена в системе.

Обратите внимание, что для создания [настраиваемых модулей слияния](configurable-merge-modules.md)требуется Mergemod.dll 2,0. Mergemod.dll версии 2,0 предоставляет расширенную функциональность во время сборки через интерфейс [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) . Этот CLSID поддерживает все существующие функции интерфейса [**имсммерже**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) , предоставляемые Mergemod.dll версии 1,0. Интерфейсом по умолчанию для объекта [**слияния**](merge-object.md) Mergemod.dll 2,0 является интерфейс **IMsmMerge2** , а не интерфейс **имсммерже** .

[Объектная модель для Mergemod.dll версии 1,0](object-model-for-mergemod-dll-version-1-0.md)

[Объектная модель для Mergemod.dll версии 2,0](object-model-for-mergemod-dll-version-2-0.md)

 

 
