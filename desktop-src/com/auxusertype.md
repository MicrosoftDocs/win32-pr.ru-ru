---
title: ауксусертипе
description: Указывает краткое отображаемое имя приложения и имена приложений.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- COM раздела реестра Ауксусертипе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772569"
---
# <a name="auxusertype"></a>ауксусертипе

Указывает краткое отображаемое имя приложения и имена приложений.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a>Комментарии

Рекомендуемая максимальная длина для *ShortDisplayName* — 15 символов. Это имя используется в меню, включая всплывающие меню.

*ApplicationName* должно содержать фактическое имя приложения (например, "Acme Draw 2,0"). Это имя используется в поле **результаты** диалогового окна Специальная **Вставка** .

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Иолеобжект:: Жетусертипе**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




