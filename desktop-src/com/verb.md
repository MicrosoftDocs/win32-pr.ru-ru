---
title: Команда
description: Указывает команды для регистрации в приложении.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Раздел реестра verb-COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105710371"
---
# <a name="verb"></a>Команда

Указывает команды для регистрации в приложении.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a>Комментарии

Каждая команда является значением **reg \_ SZ** в форме "*имя*, *\_ флаг меню*, *\_ флаг команды*". Глаголы должны быть пронумерованы последовательно.

*Имя* описывает, как команда добавляется вызовом функции [**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua) . Например, "&Play".

Значение *\_ флага меню* указывает, как команда должна отображаться в меню. Поддерживаются все флаги, поддерживаемые [**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua) , за исключением \_ всплывающего изображения MF, MF \_ овнердрав и MF \_ .

Значение *\_ флага команды* описывает атрибуты команд. Используйте одно из значений из [**олевербаттриб**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)или 0.

Дополнительные сведения см. в статьях [**олеверб**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**Иолеобжект::D оверб**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)и [**иолеобжект:: енумвербс**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**олеверб**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**олевербаттриб**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 