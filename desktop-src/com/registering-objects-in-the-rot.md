---
title: Регистрация объектов в таблице ROT
description: Регистрация объектов в таблице ROT
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d77e7bc6fe8b0a4d5896bf33575df2f57fb0e583f78acd02653f6ccb014f34ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104819"
---
# <a name="registering-objects-in-the-rot"></a>Регистрация объектов в таблице ROT

Как правило, когда клиент запрашивает у сервера создание экземпляра объекта, сервер обычно создает моникер для объекта и регистрирует его в запущенной таблице объектов (ROT) с помощью вызова [**ируннингобжекттабле:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register).

Когда сервер вызывает [**креатефилемоникер**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) для создания специального имени файла для регистрации в таблице ROT, серверы должны передавать локальные имена файлов, которые хранятся на диске, а не в формате UNC. Это гарантирует, что данные сравнения моникера, создаваемые вызовом регистрации ROT, будут соответствовать тому, что используется при поиске в таблице ROT для части удаленного клиента. Это происходит потому, что когда распределенная служба COM получает запрос на активацию файла, расположенного на локальном сервере, от удаленного клиента, файл преобразуется в путь на локальном диске.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Установка в качестве приложения службы](installing-as-a-service-application.md)
</dt> <dt>

[Регистрация класса при установке](registering-a-class-at-installation.md)
</dt> <dt>

[Регистрация работающего сервера EXE](registering-a-running-exe-server.md)
</dt> <dt>

[Самостоятельная регистрация](self-registration.md)
</dt> </dl>

 

 




