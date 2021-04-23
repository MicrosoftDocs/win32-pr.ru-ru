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
# <a name="adding-an-attachment-snap-in-extension-node"></a><span data-ttu-id="6c191-103">Добавление узла расширения оснастки «вложение»</span><span class="sxs-lookup"><span data-stu-id="6c191-103">Adding an Attachment Snap-in Extension Node</span></span>

<span data-ttu-id="6c191-104">Расширение оснастки вложений должно добавлять себя в узел службы, когда этот узел развертывается пользователем.</span><span class="sxs-lookup"><span data-stu-id="6c191-104">An attachment snap-in extension must add itself under the Services node when that node is expanded by a user.</span></span>

<span data-ttu-id="6c191-105">Когда пользователь развертывает узел службы в одной из оснасток настройки безопасности, MMC использует [**икомпонентдата:: notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) и ммкн \_ expand уведомление, чтобы уведомить оснастку настройки безопасности, а также все его расширения.</span><span class="sxs-lookup"><span data-stu-id="6c191-105">When a user expands the Services node under one of the Security Configuration snap-ins, MMC uses [**IComponentData::Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) and the MMCN\_EXPAND notification message to notify the Security Configuration snap-in, plus all its extensions.</span></span>

<span data-ttu-id="6c191-106">Затем оснастка настройки безопасности извлекает внутренний формат из *лпдатаобжект*, который передается из основной платформы MMC в качестве типа **лпдатаобжект**.</span><span class="sxs-lookup"><span data-stu-id="6c191-106">The Security Configuration snap-in then extracts its internal format from the *lpDataObject*, which is passed in from the MMC main framework as type **LPDATAOBJECT**.</span></span> <span data-ttu-id="6c191-107">Он останавливает обработку, когда видит тип узла служб.</span><span class="sxs-lookup"><span data-stu-id="6c191-107">It stops processing when it sees the Services node type.</span></span> <span data-ttu-id="6c191-108">Затем расширение оснастки вложения Извлекает тип узла из *лпдатаобжект*.</span><span class="sxs-lookup"><span data-stu-id="6c191-108">The attachment snap-in extension then extracts the node type from the *lpDataObject*.</span></span> <span data-ttu-id="6c191-109">Если тип узла является одним из типов определенных узлов службы, расширение оснастки вложений вставляет свои корневые узлы в указанный родительский узел.</span><span class="sxs-lookup"><span data-stu-id="6c191-109">If the node type is one of the service's defined node types, the attachment snap-in extension inserts its root nodes under the specified parent node.</span></span>

<span data-ttu-id="6c191-110">Обратите внимание, что в этом примере Екстрактнодетипе является закрытой функцией, реализуемой расширением.</span><span class="sxs-lookup"><span data-stu-id="6c191-110">Note that in this example, ExtractNodeType, is a private function that the extension implements.</span></span> <span data-ttu-id="6c191-111">Расширение проверяет объект данных для получения типа узла.</span><span class="sxs-lookup"><span data-stu-id="6c191-111">The extension examines the data object to get the node type.</span></span> <span data-ttu-id="6c191-112">Реализация Екстрактнодетипе не показана.</span><span class="sxs-lookup"><span data-stu-id="6c191-112">The implementation of ExtractNodeType is not shown.</span></span>


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



 

 
