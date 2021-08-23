---
title: Проверка регистрации
description: Проверка регистрации
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d7f03f1d76b780b49bec5d744a02beca9a3dc45417bf8c6efddd8ff5a9e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501654"
---
# <a name="checking-registration"></a>Проверка регистрации

При каждой загрузке приложения необходимо проверить его регистрацию, чтобы определить следующее:

-   Содержатся ли в реестре идентификаторы CLSID. Если они отсутствуют, приложение должно зарегистрироваться в качестве исходной установки.
-   Имеются ли в регистре CLSID приложения, но не имеющие в них сведений, относящихся к OLE 2. В этом случае приложение должно зарегистрироваться в качестве исходной установки.
-   Указывает, указывают ли путь, содержащий записи сервера ([локалсервер](localserver.md) и [LocalServer32](localserver32.md), [Инпроксервер](inprocserver.md) и [InprocServer32](inprocserver32.md), и [дефаултикон](defaulticon.md)), на расположение, в котором приложение в настоящий момент установлено. Если путь не имеет, перепишите записи пути, чтобы они указывали на текущее расположение.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистрация приложений COM](registering-com-applications.md)
</dt> </dl>

 

 




