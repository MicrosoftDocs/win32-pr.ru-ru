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
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412856"
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

 

 