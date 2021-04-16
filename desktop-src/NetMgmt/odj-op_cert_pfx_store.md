---
title: OP_CERT_PFX_STORE
description: Определение OP_CERT_PFX_STORE IDL
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "105719168"
---
# <a name="op_cert_pfx_store-structure"></a><span data-ttu-id="93c80-103">Структура OP_CERT_PFX_STORE</span><span class="sxs-lookup"><span data-stu-id="93c80-103">OP_CERT_PFX_STORE structure</span></span>

<span data-ttu-id="93c80-104">Содержит сериализованную структуру PFX.</span><span class="sxs-lookup"><span data-stu-id="93c80-104">Contains a serialized PFX structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93c80-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a><span data-ttu-id="93c80-106">Члены</span><span class="sxs-lookup"><span data-stu-id="93c80-106">Members</span></span>

### <a name="ptemplatename"></a><span data-ttu-id="93c80-107">птемплатенаме</span><span class="sxs-lookup"><span data-stu-id="93c80-107">pTemplateName</span></span>

<span data-ttu-id="93c80-108">Необходимо задать имя шаблона сертификата, используемого для создания сертификата.</span><span class="sxs-lookup"><span data-stu-id="93c80-108">Must be set to the name of the certificate template used to create the certificate.</span></span>

### <a name="ulprivatekeyexportpolicy"></a><span data-ttu-id="93c80-109">улприватекэйекспортполици</span><span class="sxs-lookup"><span data-stu-id="93c80-109">ulPrivateKeyExportPolicy</span></span>

<span data-ttu-id="93c80-110">Содержит одно значение из перечисления [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) .</span><span class="sxs-lookup"><span data-stu-id="93c80-110">Contains one value from the [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) enumeration.</span></span>

### <a name="ppolicyserverurl"></a><span data-ttu-id="93c80-111">пполицисерверурл</span><span class="sxs-lookup"><span data-stu-id="93c80-111">pPolicyServerUrl</span></span>

<span data-ttu-id="93c80-112">Необходимо задать URL-адрес сервера политики.</span><span class="sxs-lookup"><span data-stu-id="93c80-112">Must be set the URL of the policy server.</span></span>

### <a name="ulpolicyserverurlflags"></a><span data-ttu-id="93c80-113">улполицисерверурлфлагс</span><span class="sxs-lookup"><span data-stu-id="93c80-113">ulPolicyServerUrlFlags</span></span>

<span data-ttu-id="93c80-114">Содержит одно значение из перечисления [**полицисерверурлфлагс**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) .</span><span class="sxs-lookup"><span data-stu-id="93c80-114">Contains one value from the [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) enumeration.</span></span>

### <a name="ppolicyserverid"></a><span data-ttu-id="93c80-115">пполицисерверид</span><span class="sxs-lookup"><span data-stu-id="93c80-115">pPolicyServerId</span></span>

<span data-ttu-id="93c80-116">Содержит строку, однозначно идентифицирующую сервер политики.</span><span class="sxs-lookup"><span data-stu-id="93c80-116">Contains a string that uniquely identifies the policy server</span></span>

### <a name="cbpfx"></a><span data-ttu-id="93c80-117">кбпфкс</span><span class="sxs-lookup"><span data-stu-id="93c80-117">cbPfx</span></span>

<span data-ttu-id="93c80-118">Содержит размер Ппфкс в байтах.</span><span class="sxs-lookup"><span data-stu-id="93c80-118">Contains the size of pPfx in bytes.</span></span>

### <a name="ppfx"></a><span data-ttu-id="93c80-119">ппфкс</span><span class="sxs-lookup"><span data-stu-id="93c80-119">pPfx</span></span>

<span data-ttu-id="93c80-120">Содержит сериализованную структуру PFX (см. [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span><span class="sxs-lookup"><span data-stu-id="93c80-120">Contains a serialized PFX structure (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="93c80-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93c80-121">See also</span></span>

[<span data-ttu-id="93c80-122">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="93c80-122">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
