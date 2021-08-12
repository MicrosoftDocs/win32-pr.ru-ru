---
title: ауксусертипе
description: Указывает краткое отображаемое имя приложения и имена приложений.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- COM раздела реестра Ауксусертипе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1dbec8e873e6f6cfcb5fdb29468c1f09c0a7a6935280054e129ddac0b49e282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550727"
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

## <a name="remarks"></a>Remarks

Рекомендуемая максимальная длина для *ShortDisplayName* — 15 символов. Это имя используется в меню, включая всплывающие меню.

*ApplicationName* должно содержать фактическое имя приложения (например, "Acme Draw 2,0"). Это имя используется в поле **результаты** диалогового окна Специальная **Вставка** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Иолеобжект:: Жетусертипе**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




