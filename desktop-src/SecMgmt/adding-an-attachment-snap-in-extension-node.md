---
description: Расширение оснастки вложений должно добавлять себя в узел службы, когда этот узел развертывается пользователем.
ms.assetid: af853c29-11c2-4fd0-ad81-80aebeb74cc3
title: Добавление узла расширения оснастки «вложение»
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2604a58284af7bc55ff57ae114bc77d8f0cd42ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815737"
---
# <a name="adding-an-attachment-snap-in-extension-node"></a>Добавление узла расширения оснастки «вложение»

Расширение оснастки вложений должно добавлять себя в узел службы, когда этот узел развертывается пользователем.

Когда пользователь развертывает узел службы в одной из оснасток настройки безопасности, MMC использует [**икомпонентдата:: notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) и ммкн \_ expand уведомление, чтобы уведомить оснастку настройки безопасности, а также все его расширения.

Затем оснастка настройки безопасности извлекает внутренний формат из *лпдатаобжект*, который передается из основной платформы MMC в качестве типа **лпдатаобжект**. Он останавливает обработку, когда видит тип узла служб. Затем расширение оснастки вложения Извлекает тип узла из *лпдатаобжект*. Если тип узла является одним из типов определенных узлов службы, расширение оснастки вложений вставляет свои корневые узлы в указанный родительский узел.

Обратите внимание, что в этом примере Екстрактнодетипе является закрытой функцией, реализуемой расширением. Расширение проверяет объект данных для получения типа узла. Реализация Екстрактнодетипе не показана.


```C++
//  Detect which extension node to expand.
GUID* nodeType = ExtractNodeType(lpdataObject);

if (NULL == nodeType)
{
  return S_OK;
}

if (TRUE == ::IsEqualGUID(*nodeType, cNodetypeSceTemplateServices))
{
  folderType = ATTACHMENT_STATIC;  // defined by attachment writer
}

else if (TRUE == ::IsEqualGUID
    (*nodeType, cNodetypeSceAnalysisServices))
{
  folderType = ATTACHMENT_STATIC_ANALYSIS;
               // defined by attachment writer
}

//  Free resources.
::GlobalFree(reinterpret_cast<HANDLE>(nodeType));

//  Add service attachment root node and remember it as the
//  root of the SMB extension namespace.
//  ...
```



 

 
