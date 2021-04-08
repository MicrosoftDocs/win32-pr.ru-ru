---
title: проксистубклсид
description: Сопоставляет идентификатор IID с идентификатором CLSID в 16-разрядных прокси-библиотеках.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- COM-значение реестра Проксистубклсид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068379"
---
# <a name="proxystubclsid"></a><span data-ttu-id="c31ce-104">проксистубклсид</span><span class="sxs-lookup"><span data-stu-id="c31ce-104">ProxyStubClsid</span></span>

<span data-ttu-id="c31ce-105">Сопоставляет идентификатор IID с идентификатором CLSID в 16-разрядных прокси-библиотеках.</span><span class="sxs-lookup"><span data-stu-id="c31ce-105">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c31ce-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="c31ce-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="c31ce-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c31ce-107">Remarks</span></span>

<span data-ttu-id="c31ce-108">Это значение **reg \_ SZ** , указывающее идентификатор CLSID для IID.</span><span class="sxs-lookup"><span data-stu-id="c31ce-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="c31ce-109">При добавлении интерфейсов необходимо использовать эту запись для их регистрации (16-разрядные системы), чтобы OLE мог найти соответствующий код удаленного взаимодействия для установления межпроцессного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="c31ce-109">If you add interfaces, you must use this entry to register them (16-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c31ce-110">См. также</span><span class="sxs-lookup"><span data-stu-id="c31ce-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c31ce-111">**Интерфейс**</span><span class="sxs-lookup"><span data-stu-id="c31ce-111">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="c31ce-112">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="c31ce-112">**ProxyStubClsid32**</span></span>](proxystubclsid32.md)
</dt> </dl>

 

 




