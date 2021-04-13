---
title: IMsRdpClientTransportSettings2 Гатевайенкриптедотпкукие, свойство
description: Указывает или получает зашифрованный файл cookie одноразового пароля (OTP).
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайенкриптедотпкукие
- Службы удаленных рабочих столов свойства Гатевайенкриптедотпкукие, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайенкриптедотпкукие
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5463d3d576144fc0a58b543904d6d4934b68c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535567"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a><span data-ttu-id="06b84-106">Свойство IMsRdpClientTransportSettings2:: Гатевайенкриптедотпкукие</span><span class="sxs-lookup"><span data-stu-id="06b84-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookie property</span></span>

<span data-ttu-id="06b84-107">Указывает или получает зашифрованный файл cookie одноразового пароля (OTP).</span><span class="sxs-lookup"><span data-stu-id="06b84-107">Specifies or retrieves the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="06b84-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="06b84-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b84-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06b84-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a><span data-ttu-id="06b84-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="06b84-110">Property value</span></span>

<span data-ttu-id="06b84-111">Указывает или получает зашифрованный файл cookie OTP.</span><span class="sxs-lookup"><span data-stu-id="06b84-111">Specifies or retrieves the encrypted OTP cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b84-112">Требования</span><span class="sxs-lookup"><span data-stu-id="06b84-112">Requirements</span></span>



| <span data-ttu-id="06b84-113">Требование</span><span class="sxs-lookup"><span data-stu-id="06b84-113">Requirement</span></span> | <span data-ttu-id="06b84-114">Значение</span><span class="sxs-lookup"><span data-stu-id="06b84-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06b84-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06b84-115">Minimum supported client</span></span><br/> | <span data-ttu-id="06b84-116">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="06b84-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="06b84-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06b84-117">Minimum supported server</span></span><br/> | <span data-ttu-id="06b84-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06b84-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="06b84-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="06b84-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="06b84-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06b84-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="06b84-121">DLL</span><span class="sxs-lookup"><span data-stu-id="06b84-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06b84-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06b84-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="06b84-123">IID</span><span class="sxs-lookup"><span data-stu-id="06b84-123">IID</span></span><br/>                      | <span data-ttu-id="06b84-124">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="06b84-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06b84-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06b84-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b84-126">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="06b84-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="06b84-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="06b84-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





