---
description: Свойство ColorKey задает или получает цветовой ключ, используемый в закрытых субтитрах.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: ColorKey, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494637"
---
# <a name="colorkey-property"></a>ColorKey, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`ColorKey`Свойство задает или получает цветовой ключ, используемый в закрытых субтитрах.

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее цвет, используемый в качестве прозрачного фона для текста с субтитрами. Значение по умолчанию в 256 Colors — пурпурный, а «выкл.-черный» — в любой другой глубине цвета.

## <a name="remarks"></a>Комментарии

Это свойство доступно для чтения и записи. Это свойство применяется только к закрытым заголовкам, если таковые существуют, а не к потоку субтитров.

 

 



