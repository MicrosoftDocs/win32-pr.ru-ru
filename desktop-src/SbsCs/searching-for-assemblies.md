---
description: Существует два метода, с помощью которых приложение размещения может искать параллельные сборки.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Поиск сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647627"
---
# <a name="searching-for-assemblies"></a>Поиск сборок

Существует два метода, с помощью которых приложение размещения может искать параллельные сборки.

Размещенные модули могут зарегистрироваться в ведущем приложении, расширяя некоторые общие сведения о конфигурации. Затем приложение может использовать эти сведения о конфигурации для загрузки сборок, необходимых для новой функциональности. Это можно сделать, вызвав [**креатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) для манифестов, указанных в регистрационных данных, а затем вызвав [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы попасть в новый модуль. Обратите внимание, что при использовании этого метода новые компоненты должны обновить некоторое состояние общего приложения, чтобы указать их присутствие.

Приложение размещения может активно искать сборки при запуске с помощью [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) и [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) , чтобы искать библиотеки DLL или манифесты в указанном расположении, а затем использовать [**креатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) для доступа к данным. Для этого метода не требуется регистрация компонента.

 

 
