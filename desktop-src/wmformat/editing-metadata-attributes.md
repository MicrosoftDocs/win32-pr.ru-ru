---
title: Изменение атрибутов метаданных
description: Изменение атрибутов метаданных
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media Format SDK, изменение атрибутов метаданных
- Расширенный системный формат (ASF), изменение атрибутов метаданных
- ASF (Расширенный системный формат), изменение атрибутов метаданных
- метаданные, изменение атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412562"
---
# <a name="editing-metadata-attributes"></a>Изменение атрибутов метаданных

Изменение атрибутов метаданных очень похоже на установку новых. Вместо использования [**IWMHeaderInfo3:: аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)используйте [**IWMHeaderInfo3:: модифяттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **Модифяттрибуте** идентичен **аддаттрибуте** , за исключением того, что не указывается имя атрибута, а номер индекса является входным параметром, а не выходным.

Можно использовать потоковый номер 0xFFFF, чтобы указать атрибут для изменения с помощью его глобального индекса.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Работа с метаданными**](working-with-metadata.md)
</dt> </dl>

 

 




