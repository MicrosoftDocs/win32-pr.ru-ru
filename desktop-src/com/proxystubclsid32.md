---
title: ProxyStubClsid32
description: Сопоставляет идентификатор IID с идентификатором CLSID в 32-разрядных прокси-библиотеках.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- COM-значение реестра ProxyStubClsid32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339369"
---
# <a name="proxystubclsid32"></a><span data-ttu-id="a1521-104">ProxyStubClsid32</span><span class="sxs-lookup"><span data-stu-id="a1521-104">ProxyStubClsid32</span></span>

<span data-ttu-id="a1521-105">Сопоставляет идентификатор IID с идентификатором CLSID в 32-разрядных прокси-библиотеках.</span><span class="sxs-lookup"><span data-stu-id="a1521-105">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a1521-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="a1521-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="a1521-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1521-107">Remarks</span></span>

<span data-ttu-id="a1521-108">Это значение **reg \_ SZ** , указывающее идентификатор CLSID для IID.</span><span class="sxs-lookup"><span data-stu-id="a1521-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="a1521-109">Это обязательная запись, поскольку сопоставление IID-to-CLSID может отличаться для 16-разрядных и 32-разрядных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="a1521-109">This is a required entry since the IID-to-CLSID mapping may be different for 16-bit and 32-bit interfaces.</span></span> <span data-ttu-id="a1521-110">Сопоставление IID с CLSID зависит от способа упаковки прокси-серверов интерфейса в набор DLL-библиотек прокси.</span><span class="sxs-lookup"><span data-stu-id="a1521-110">The IID-to-CLSID mapping depends on the way the interface proxies are packaged into a set of proxy DLLs.</span></span>

<span data-ttu-id="a1521-111">При добавлении интерфейсов необходимо использовать эту запись для их регистрации (32-разрядные системы), чтобы OLE мог найти соответствующий код удаленного взаимодействия для установления межпроцессного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a1521-111">If you add interfaces, you must use this entry to register them (32-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1521-112">См. также</span><span class="sxs-lookup"><span data-stu-id="a1521-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1521-113">**IMarshal**</span><span class="sxs-lookup"><span data-stu-id="a1521-113">**IMarshal**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[<span data-ttu-id="a1521-114">**Интерфейс**</span><span class="sxs-lookup"><span data-stu-id="a1521-114">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="a1521-115">**проксистубклсид**</span><span class="sxs-lookup"><span data-stu-id="a1521-115">**ProxyStubClsid**</span></span>](proxystubclsid.md)
</dt> </dl>

 

 