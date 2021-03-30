---
title: Регистрация объектов в таблице ROT
description: Регистрация объектов в таблице ROT
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b452ead94a717791910ecceaa5082535bc1b233c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410999"
---
# <a name="registering-objects-in-the-rot"></a>Регистрация объектов в таблице ROT

Как правило, когда клиент запрашивает у сервера создание экземпляра объекта, сервер обычно создает моникер для объекта и регистрирует его в запущенной таблице объектов (ROT) с помощью вызова [**ируннингобжекттабле:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register).

Когда сервер вызывает [**креатефилемоникер**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) для создания специального имени файла для регистрации в таблице ROT, серверы должны передавать локальные имена файлов, которые хранятся на диске, а не в формате UNC. Это гарантирует, что данные сравнения моникера, создаваемые вызовом регистрации ROT, будут соответствовать тому, что используется при поиске в таблице ROT для части удаленного клиента. Это происходит потому, что когда распределенная служба COM получает запрос на активацию файла, расположенного на локальном сервере, от удаленного клиента, файл преобразуется в путь на локальном диске.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Установка в качестве приложения службы](installing-as-a-service-application.md)
</dt> <dt>

[Регистрация класса при установке](registering-a-class-at-installation.md)
</dt> <dt>

[Регистрация работающего сервера EXE](registering-a-running-exe-server.md)
</dt> <dt>

[Самостоятельная регистрация](self-registration.md)
</dt> </dl>

 

 




