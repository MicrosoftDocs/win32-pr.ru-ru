---
title: IMsRdpClientTransportSettings3 Гатевайенкриптедаускукиесизе, свойство
description: Размер (в символах) свойства Гатевайенкриптедаускукие.
ms.assetid: 52e24bef-5afa-4954-b639-08ea8701404a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайенкриптедаускукиесизе
- Службы удаленных рабочих столов свойства Гатевайенкриптедаускукиесизе, интерфейс IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, свойство Гатевайенкриптедаускукиесизе
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238245cdb9c0164b69434cf61f790b8f81fa3da2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491331"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookiesize-property"></a><span data-ttu-id="2d4c9-106">Свойство IMsRdpClientTransportSettings3:: Гатевайенкриптедаускукиесизе</span><span class="sxs-lookup"><span data-stu-id="2d4c9-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookieSize property</span></span>

<span data-ttu-id="2d4c9-107">Размер (в символах) свойства [**гатевайенкриптедаускукие**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .</span><span class="sxs-lookup"><span data-stu-id="2d4c9-107">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span>

<span data-ttu-id="2d4c9-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2d4c9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d4c9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d4c9-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookieSize(
  [in]          ULONG ulEncryptedAuthCookieSize
);

HRESULT get_GatewayEncryptedAuthCookieSize(
  [out, retval] ULONG *ulEncryptedAuthCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="2d4c9-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2d4c9-110">Property value</span></span>

<span data-ttu-id="2d4c9-111">Значение типа **ulong** , содержащее новое значение размера.</span><span class="sxs-lookup"><span data-stu-id="2d4c9-111">A **ULONG** value that contains the new size value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d4c9-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2d4c9-112">Requirements</span></span>



| <span data-ttu-id="2d4c9-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2d4c9-113">Requirement</span></span> | <span data-ttu-id="2d4c9-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2d4c9-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d4c9-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d4c9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2d4c9-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d4c9-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="2d4c9-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d4c9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2d4c9-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d4c9-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2d4c9-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2d4c9-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d4c9-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d4c9-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2d4c9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2d4c9-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d4c9-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d4c9-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d4c9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d4c9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d4c9-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="2d4c9-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





