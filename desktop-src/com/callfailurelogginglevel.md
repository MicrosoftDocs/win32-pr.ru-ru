---
title: каллфаилурелоггинглевел
description: Задает уровень детализации записей журнала событий о неудачных вызовах компонентов.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- COM-значение реестра Каллфаилурелоггинглевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888123"
---
# <a name="callfailurelogginglevel"></a>каллфаилурелоггинглевел

Задает уровень детализации записей журнала событий о неудачных вызовах компонентов.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ DWORD** .



| Значение | Описание                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Всегда заносить в журнал ошибки во время вызова в процессе COM-сервера.                           |
| 2     | Не заносить в журнал сбои во время вызова в процессе COM-сервера. Это значение по умолчанию. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка безопасности для приложений COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




