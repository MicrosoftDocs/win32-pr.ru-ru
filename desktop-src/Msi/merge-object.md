---
description: Объект Merge предоставляет доступ к другим объектам верхнего уровня. Перед загрузкой поддержки автоматизации, необходимой COM для доступа к функциям в Mergemod.dll, необходимо создать объект слияния.
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: Объект Merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1379202d4f252560a381f8af09b30741faa060ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272607"
---
# <a name="merge-object"></a>Объект Merge

Объект **Merge** предоставляет доступ к другим объектам верхнего уровня. Перед загрузкой поддержки автоматизации, необходимой COM для доступа к функциям в Mergemod.dll, необходимо создать объект **слияния** .

Mergemod.dll предоставляет доступ к расширенным функциям во время сборки с помощью второй версии существующего идентификатора CLSID. Этот CLSID поддерживает существующие функции, доступные через интерфейс [**имсммерже**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) , но интерфейс по умолчанию для объекта (и связанный с ним сдвоенный интерфейс) является интерфейсом [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) , а не интерфейсом **имсммерже** .

 

 
