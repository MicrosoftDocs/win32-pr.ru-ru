---
title: IMsRdpClientTransportSettings2 Гатевайенкриптедотпкукиесизе, свойство
description: Указывает или получает размер зашифрованного файла cookie одноразового пароля (OTP).
ms.assetid: a4fdcd06-59ae-407f-9ac6-dfe4b52fb5d7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайенкриптедотпкукиесизе
- Службы удаленных рабочих столов свойства Гатевайенкриптедотпкукиесизе, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайенкриптедотпкукиесизе
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e714b7c03e898b29b1ae02e3b19d65fde8dfcb91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802153"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookiesize-property"></a><span data-ttu-id="4fa26-106">Свойство IMsRdpClientTransportSettings2:: Гатевайенкриптедотпкукиесизе</span><span class="sxs-lookup"><span data-stu-id="4fa26-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookieSize property</span></span>

<span data-ttu-id="4fa26-107">Указывает или получает размер зашифрованного файла cookie одноразового пароля (OTP).</span><span class="sxs-lookup"><span data-stu-id="4fa26-107">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="4fa26-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4fa26-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa26-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fa26-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookieSize(
  [in]  ULONG ulEncryptedOtpCookieSize
);

HRESULT get_GatewayEncryptedOtpCookieSize(
  [out] ULONG *pulEncryptedOtpCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="4fa26-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4fa26-110">Property value</span></span>

<span data-ttu-id="4fa26-111">Указывает или получает размер зашифрованного файла cookie одноразового пароля (OTP).</span><span class="sxs-lookup"><span data-stu-id="4fa26-111">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa26-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4fa26-112">Requirements</span></span>



| <span data-ttu-id="4fa26-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4fa26-113">Requirement</span></span> | <span data-ttu-id="4fa26-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4fa26-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa26-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fa26-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4fa26-116">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="4fa26-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="4fa26-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fa26-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4fa26-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fa26-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="4fa26-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4fa26-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fa26-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fa26-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4fa26-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4fa26-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fa26-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fa26-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4fa26-123">IID</span><span class="sxs-lookup"><span data-stu-id="4fa26-123">IID</span></span><br/>                      | <span data-ttu-id="4fa26-124">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="4fa26-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4fa26-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fa26-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa26-126">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="4fa26-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="4fa26-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="4fa26-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





