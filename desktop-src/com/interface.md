---
title: Interface (COM)
description: Необязательная запись, указывающая все идентификаторы интерфейса (идентификаторов IID), поддерживаемые связанным классом.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Раздел реестра интерфейса COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710430"
---
# <a name="interface-com"></a><span data-ttu-id="6672e-104">Interface (COM)</span><span class="sxs-lookup"><span data-stu-id="6672e-104">Interface (COM)</span></span>

<span data-ttu-id="6672e-105">Необязательная запись, указывающая все идентификаторы интерфейса (идентификаторов IID), поддерживаемые связанным классом.</span><span class="sxs-lookup"><span data-stu-id="6672e-105">An optional entry that specifies all interface IDs (IIDs) supported by the associated class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6672e-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="6672e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a><span data-ttu-id="6672e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6672e-107">Remarks</span></span>

<span data-ttu-id="6672e-108">Если имя интерфейса отсутствует в этом списке, интерфейс не может поддерживаться экземпляром этого класса.</span><span class="sxs-lookup"><span data-stu-id="6672e-108">If an interface name is not present in this list, the interface can never be supported by an instance of this class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6672e-109">См. также</span><span class="sxs-lookup"><span data-stu-id="6672e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6672e-110">Ключ интерфейса</span><span class="sxs-lookup"><span data-stu-id="6672e-110">Interface Key</span></span>](interface-key.md)
</dt> </dl>

 

 




