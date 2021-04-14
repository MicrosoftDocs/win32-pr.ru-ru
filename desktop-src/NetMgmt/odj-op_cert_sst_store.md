---
title: OP_CERT_SST_STORE
description: Определение OP_CERT_SST_STORE IDL
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104414309"
---
# <a name="op_cert_sst_store-structure"></a><span data-ttu-id="33401-103">Структура OP_CERT_SST_STORE</span><span class="sxs-lookup"><span data-stu-id="33401-103">OP_CERT_SST_STORE structure</span></span>

<span data-ttu-id="33401-104">Содержит сериализованное хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="33401-104">Contains a serialized certificate store.</span></span>

## <a name="syntax"></a><span data-ttu-id="33401-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33401-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a><span data-ttu-id="33401-106">Члены</span><span class="sxs-lookup"><span data-stu-id="33401-106">Members</span></span>

### <a name="storelocation"></a><span data-ttu-id="33401-107">StoreLocation</span><span class="sxs-lookup"><span data-stu-id="33401-107">StoreLocation</span></span>

<span data-ttu-id="33401-108">Содержит идентификатор для хранилища сертификатов из [**расположений системных хранилищ**](../seccrypto/system-store-locations.md).</span><span class="sxs-lookup"><span data-stu-id="33401-108">Contains an identifier for the certificate store from [**System Store Locations**](../seccrypto/system-store-locations.md).</span></span>

### <a name="pstorename"></a><span data-ttu-id="33401-109">псторенаме</span><span class="sxs-lookup"><span data-stu-id="33401-109">pStoreName</span></span>

<span data-ttu-id="33401-110">Содержит имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="33401-110">Contains the name of the store.</span></span>

### <a name="cbsst"></a><span data-ttu-id="33401-111">кбсст</span><span class="sxs-lookup"><span data-stu-id="33401-111">cbSst</span></span>

<span data-ttu-id="33401-112">Содержит размер ПССТ в байтах.</span><span class="sxs-lookup"><span data-stu-id="33401-112">Contains the size of pSst in bytes.</span></span>

### <a name="psst"></a><span data-ttu-id="33401-113">псст</span><span class="sxs-lookup"><span data-stu-id="33401-113">pSst</span></span>

<span data-ttu-id="33401-114">Содержит сериализованное хранилище сертификатов (см. [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span><span class="sxs-lookup"><span data-stu-id="33401-114">Contains a serialized certificate store (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="33401-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33401-115">See also</span></span>

[<span data-ttu-id="33401-116">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="33401-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)