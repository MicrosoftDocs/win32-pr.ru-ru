---
title: IMsRdpClientTransportSettings3 Гатевайкредсаурцекукие, свойство
description: Указывает, является ли источник учетных данных основанным на файлах cookie.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайкредсаурцекукие
- Службы удаленных рабочих столов свойства Гатевайкредсаурцекукие, интерфейс IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, свойство Гатевайкредсаурцекукие
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672865"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a><span data-ttu-id="d25c7-106">Свойство IMsRdpClientTransportSettings3:: Гатевайкредсаурцекукие</span><span class="sxs-lookup"><span data-stu-id="d25c7-106">IMsRdpClientTransportSettings3::GatewayCredSourceCookie property</span></span>

<span data-ttu-id="d25c7-107">Указывает, является ли источник учетных данных основанным на файлах cookie.</span><span class="sxs-lookup"><span data-stu-id="d25c7-107">Specifies if the credential source is cookie based.</span></span> <span data-ttu-id="d25c7-108">Содержит один, если источник учетных данных основан на файлах cookie или в противном случае — ноль.</span><span class="sxs-lookup"><span data-stu-id="d25c7-108">Contains one if the credential source is cookie-based or zero otherwise.</span></span>

<span data-ttu-id="d25c7-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d25c7-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d25c7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d25c7-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a><span data-ttu-id="d25c7-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d25c7-111">Property value</span></span>

<span data-ttu-id="d25c7-112">Значение типа **ulong** , указывающее, является ли источник учетных данных основанным на файлах cookie.</span><span class="sxs-lookup"><span data-stu-id="d25c7-112">A **ULONG** value that specifies if the credential source is cookie based.</span></span>

## <a name="requirements"></a><span data-ttu-id="d25c7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d25c7-113">Requirements</span></span>



| <span data-ttu-id="d25c7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d25c7-114">Requirement</span></span> | <span data-ttu-id="d25c7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d25c7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d25c7-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d25c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d25c7-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d25c7-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="d25c7-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d25c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d25c7-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d25c7-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d25c7-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d25c7-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d25c7-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d25c7-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d25c7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d25c7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d25c7-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d25c7-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d25c7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d25c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25c7-125">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="d25c7-125">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





