---
title: Ресурс меню
description: Определяет содержимое ресурса меню. | Ресурс меню
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- МЕНЮ ресурсов MENU и другие ресурсы
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713422"
---
# <a name="menu-resource"></a>Ресурс меню

Определяет содержимое ресурса меню. Ресурс меню — это коллекция сведений, определяющих внешний вид и функции меню приложения. Меню — это специальное средство ввода, которое позволяет пользователю выбирать команды и открывать подменю из списка пунктов меню.

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*менуид*
</dt> <dd>

Число, идентифицирующее меню. Это значение является уникальной строкой или уникальным 16-битовым целочисленным значением без знака в диапазоне от 1 до 65 535.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*Необязательные операторы*
</dt> <dd>

Этот параметр может быть больше нуля из следующих инструкций.



| Инструкция                                                        | Описание                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Параметры**](characteristics-statement.md) *DWORD*     | Определяемая пользователем информация о ресурсе, который может использоваться средствами чтения и записи файлов ресурсов. Дополнительные сведения см. в разделе [**характеристики**](characteristics-statement.md). |
| [](language-statement.md) *Язык* языка, *подязык* | Язык для ресурса. Дополнительные сведения см. в разделе [**Language**](language-statement.md).                                                                                            |
| [**Версия**](version-statement.md) *DWORD*                     | Определяемый пользователем номер версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов. Дополнительные сведения см. в разделе [**версия**](version-statement.md).              |



 

</dd> </dl>

Для обратной совместимости также поддерживаются некоторые атрибуты. Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).

## <a name="examples"></a>Примеры

Ниже приведен пример полного оператора **меню** :

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование меню](./using-menus.md)
</dt> <dt>

[**Accelerator**](accelerators-resource.md)
</dt> <dt>

[**ПОКАЗАТЕЛИ**](characteristics-statement.md)
</dt> <dt>

[**ЯЗЫКЕ**](language-statement.md)
</dt> <dt>

[**менуекс**](menuex-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**ПОДСКАЗКИ**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Версия**](version-statement.md)
</dt> </dl>

 

 
