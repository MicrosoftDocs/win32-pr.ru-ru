---
title: каллфаилурелоггинглевел
description: Задает уровень детализации записей журнала событий о неудачных вызовах компонентов.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- COM-значение реестра Каллфаилурелоггинглевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819d132a8cd0f1741eb3b825a17f02387b200e80f2dba6913821e77f9a0913cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793824"
---
# <a name="callfailurelogginglevel"></a>каллфаилурелоггинглевел

Задает уровень детализации записей журнала событий о неудачных вызовах компонентов.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ DWORD** .



| Значение | Описание                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Всегда заносить в журнал ошибки во время вызова в процессе COM-сервера.                           |
| 2     | Не заносить в журнал сбои во время вызова в процессе COM-сервера. Это значение по умолчанию. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка безопасности для приложений COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




