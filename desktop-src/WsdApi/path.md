---
description: Указывает расположение и имя файла WSDL. Путь может быть абсолютным или относительным путем к файлу, но не должен быть URL-адресом.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: элемент Path (веб-службы на устройствах)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3597248a2cbead5afdeb2fd1cd41613e1c4617b7be1ea636abb3ddbd2cdc92be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071424"
---
# <a name="path-element"></a>элемент Path

Указывает расположение и имя файла WSDL. Путь может быть абсолютным или относительным путем к файлу, но не должен быть URL-адресом.

## <a name="usage"></a>Использование

``` syntax
<path/>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                         | Описание                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [**файле**](wsdl.md)<br/> | WSDL-файл для обработки сведений о контракте.<br/> <br/> |



## <a name="examples"></a>Примеры

В следующем XML-коде показан допустимый элемент **path** .

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a>Сведения об элементе



| Метка | Значение |
|-------------------------------------|---------------|
| Минимальная поддерживаемая система<br/> | Windows Vista |
| Может быть пустым                        | Да           |



 

 




