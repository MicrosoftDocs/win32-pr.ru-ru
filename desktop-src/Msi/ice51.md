---
description: ICE51 проверяет, предоставлено ли название для файлов ресурсов шрифтов.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265832"
---
# <a name="ice51"></a>ICE51

ICE51 проверяет, предоставлено ли название для файлов ресурсов шрифтов.

Необходимо указать заголовок для ресурса шрифта, который не имеет внедренного имени. Для файлов ресурсов шрифта. ТТК,. ttf и. ОТФ не требуется заголовок, так как эти файлы содержат внедренное имя. Не следует указывать заголовок для ресурса шрифта, содержащего внедренное имя, так как система затем регистрирует шрифт дважды.

**[Установщик Windows 4,5 и более ранних версий](not-supported-in-windows-installer-4-5.md):** ICE51 не проверяет файлы ресурсов шрифтов ОТФ.

## <a name="result"></a>Результат

ICE51 отправляет сообщение об ошибке, если существуют файлы ресурсов шрифтов. ТТК,. ttf и. ОТФ с заголовками. ICE51 отправляет предупреждение, если есть другие файлы ресурсов шрифтов без заголовка.

## <a name="example"></a>Пример

ICE51 сообщит о следующем предупреждении для показанного примера.

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

ICE51 выдаст следующее сообщение об ошибке для приведенного примера.

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

[Таблица файлов](file-table.md) (частичная)



| Файл  | FileName  |
|-------|-----------|
| Font1 | font1. ttf |
| Font2 | font2. FON |



 

[Таблица шрифтов](font-table.md)



| Файл\_ | фонттитле          |
|--------|--------------------|
| Font1  | Очень крутой шрифт |
| Font2  |                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



