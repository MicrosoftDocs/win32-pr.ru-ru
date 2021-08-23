---
title: Изменение атрибутов метаданных
description: Изменение атрибутов метаданных
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Пакет SDK для формата мультимедиа, изменение атрибутов метаданных
- Расширенный системный формат (ASF), изменение атрибутов метаданных
- ASF (Расширенный системный формат), изменение атрибутов метаданных
- метаданные, изменение атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973b787b37bbf9333a0adb218ab5db0e6f677521f1bfc9a0cdc1d5c37200e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586064"
---
# <a name="editing-metadata-attributes"></a>Изменение атрибутов метаданных

Изменение атрибутов метаданных очень похоже на установку новых. Вместо использования [**IWMHeaderInfo3:: аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)используйте [**IWMHeaderInfo3:: модифяттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **Модифяттрибуте** идентичен **аддаттрибуте** , за исключением того, что не указывается имя атрибута, а номер индекса является входным параметром, а не выходным.

Можно использовать потоковый номер 0xFFFF, чтобы указать атрибут для изменения с помощью его глобального индекса.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Работа с метаданными**](working-with-metadata.md)
</dt> </dl>

 

 




