---
title: IMsRdpClientTransportSettings3 Гатевайенкриптедаускукие, свойство
description: Зашифрованный файл cookie проверки подлинности.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайенкриптедаускукие
- Службы удаленных рабочих столов свойства Гатевайенкриптедаускукие, интерфейс IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, свойство Гатевайенкриптедаускукие
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340685"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a><span data-ttu-id="89fdb-106">Свойство IMsRdpClientTransportSettings3:: Гатевайенкриптедаускукие</span><span class="sxs-lookup"><span data-stu-id="89fdb-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookie property</span></span>

<span data-ttu-id="89fdb-107">Зашифрованный файл cookie проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="89fdb-107">The encrypted authentication cookie.</span></span> <span data-ttu-id="89fdb-108">Размер свойства задается свойством [**гатевайенкриптедаускукиесизе**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) .</span><span class="sxs-lookup"><span data-stu-id="89fdb-108">The size of the property is specified by the [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) property.</span></span>

<span data-ttu-id="89fdb-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="89fdb-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fdb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89fdb-110">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a><span data-ttu-id="89fdb-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="89fdb-111">Property value</span></span>

<span data-ttu-id="89fdb-112">Новый зашифрованный файл cookie проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="89fdb-112">The new encrypted authentication cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="89fdb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="89fdb-113">Requirements</span></span>



| <span data-ttu-id="89fdb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="89fdb-114">Requirement</span></span> | <span data-ttu-id="89fdb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="89fdb-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89fdb-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89fdb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="89fdb-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89fdb-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="89fdb-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89fdb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="89fdb-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89fdb-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="89fdb-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="89fdb-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="89fdb-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89fdb-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="89fdb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="89fdb-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89fdb-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89fdb-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89fdb-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89fdb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89fdb-125">**гатевайенкриптедаускукиесизе**</span><span class="sxs-lookup"><span data-stu-id="89fdb-125">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[<span data-ttu-id="89fdb-126">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="89fdb-126">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





