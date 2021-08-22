---
title: Ресурс ТОЧЕЧного рисунка
description: Определяет точечный рисунок, используемый приложением на экране экрана или в виде элемента в меню или элементе управления.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Меню ресурсов ТОЧЕЧных РИСУНКов и другие ресурсы
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff75f235e8aa1787e93f9420b4d7ed27f440cdc09510547295ebced4ec494bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734902"
---
# <a name="bitmap-resource"></a>Ресурс ТОЧЕЧного рисунка

Определяет точечный рисунок, используемый приложением на экране экрана или в виде элемента в меню или элементе управления.

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Уникальное имя или 16-разрядное целочисленное значение без знака, идентифицирующее ресурс.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*файлов*
</dt> <dd>

Имя файла, содержащего ресурс. Имя должно быть допустимым именем файла; Он должен быть полным путем, если файл не находится в текущем рабочем каталоге. Путь должен представлять собой строку в кавычках.

</dd> </dl>

Для обратной совместимости также поддерживаются некоторые атрибуты. Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).

## <a name="examples"></a>Примеры

В следующем примере определяются два ресурса точечного рисунка:

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование точечных рисунков](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[**лоадимаже**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 